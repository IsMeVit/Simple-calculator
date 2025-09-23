<script>
export default {
  name: 'Calculator',
  data() {
    return {
      inputStr: '0', 
    };
  },
  methods: {
    updateDisplay(val) {
      const maxDigits = 12; 
      
      if (this.inputStr === '0' && !isNaN(val)) {
        this.inputStr = String(val);
      } 
      else if (this.inputStr.length < maxDigits) {
        this.inputStr += String(val);
      }
    },
    calculate() {
      try {
        this.inputStr = eval(this.inputStr).toString();
      } catch {
        this.inputStr = 'Error';
      }
    },
    clearDisplay() {
      this.inputStr = '0';
    },
    backspace() {
      if (this.inputStr.length > 1) {
        this.inputStr = this.inputStr.slice(0, -1);
      } else {
        this.inputStr = '0'; 
      }
    }
  }
};
</script>

<style scoped>
button {
  transition: background-color 0.2s ease;
}
</style>

<template>
  <div class="min-h-screen text-white flex flex-col items-center justify-center font-mono bg-[#458588]">
    <div class="text-center mb-6">
      <h1 style="color: #f9f5d7; font-size: 1.9rem;">Simple UI Calculator using Vue.js and Tailwind CSS</h1>
    </div>

    <div class="bg-[#3c3836] rounded-2xl p-7 w-[350px]">
      <div class="bg-[#504945] text-right px-4 py-3 rounded mb-4 text-2xl text-[#ebdbb2] overflow-hidden">
        {{ inputStr }}
      </div>

      <div class="grid grid-cols-4 gap-3">
        <button @click="clearDisplay" class="bg-[#cc241d] hover:bg-[#fb4934] text-white py-3 rounded">C</button>
        <button @click="backspace" class="bg-[#d3869b] hover:bg-[#b16286] text-white py-3 rounded">
          ⌫
        </button>
        <button @click="updateDisplay('/')" class="bg-[#fabd2f] hover:bg-[#d79921] text-black py-3 rounded">/</button>
        <button @click="updateDisplay('*')" class="bg-[#fabd2f] hover:bg-[#d79921] text-black py-3 rounded">×</button>

        <button v-for="n in ['7','8','9']" :key="n"
          @click="updateDisplay(n)"
          class="bg-[#689d6a] hover:bg-[#8ec07c] py-3 rounded"
        >
          {{ n }}
        </button>
        <button @click="updateDisplay('-')" class="bg-[#fabd2f] hover:bg-[#d79921] text-black py-3 rounded">−</button>

        <button v-for="n in ['4','5','6']" :key="n"
          @click="updateDisplay(n)"
          class="bg-[#689d6a] hover:bg-[#8ec07c] py-3 rounded"
        >
          {{ n }}
        </button>
        <button @click="updateDisplay('+')" class="bg-[#fabd2f] hover:bg-[#d79921] text-black py-3 rounded">+</button>

        <button v-for="n in ['1','2','3']" :key="n"
          @click="updateDisplay(n)"
          class="bg-[#689d6a] hover:bg-[#8ec07c] py-3 rounded"
        >
          {{ n }}
        </button>
        <button @click="updateDisplay('.')" class="bg-[#665c54] hover:bg-[#7c6f64] py-3 rounded">.</button>

        <button @click="updateDisplay('0')" class="col-span-2 bg-[#689d6a] hover:bg-[#8ec07c] py-3 rounded">0</button>
        <button @click="calculate" class="col-span-2 bg-[#b8bb26] hover:bg-[#a9b665] text-black py-3 rounded font-bold">=</button>
      </div>
    </div>
  </div>
</template>