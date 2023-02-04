<script>
  let firstNumber = 0;
  let secondNumber = 0;
</script>

<h1 class="text-2xl text-center font-bold">
  lesson 3: Math Operations On Numbers
</h1>

<div>
  <label for="number1">Input first Number:</label>
  <input
    class="w-[100px]"
    name="number1"
    type="number"
    bind:value={firstNumber}
  />
  <label for="number2">Input second Number:</label>
  <input
    class="w-[100px]"
    name="number2"
    type="number"
    bind:value={secondNumber}
  />
  <!-- <div> -->
  <!--   sum of these numbers: {firstNumber + secondNumber} -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   difference of these numbers: {firstNumber - -->
  <!--     secondNumber} -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   division of these numbers: {firstNumber / secondNumber} -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   product of these numbers: {firstNumber * secondNumber} -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   remainder of these numbers: {firstNumber % secondNumber} -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   <button -->
  <!--     class="rounded px-2 m-2 text-white bg-purple-900" -->
  <!--     on:click={() => -->
  <!--       (firstNumber = firstNumber + secondNumber)} -->
  <!--   > -->
  <!--     compound assignment with augmented addition -->
  <!--   </button> -->

  <!--   <button -->
  <!--     class="rounded px-2 m-2 text-white bg-purple-900" -->
  <!--     on:click={() => (firstNumber += secondNumber)} -->
  <!--   > -->
  <!--     += version -->
  <!--   </button> -->
  <!-- </div> -->

  <!-- <div> -->
  <!--   <button -->
  <!--     class="rounded px-2 m-2 text-white bg-purple-900" -->
  <!--     on:click={() => -->
  <!--       (firstNumber = firstNumber - secondNumber)} -->
  <!--   > -->
  <!--     compound assignment with augmented subtraction -->
  <!--   </button> -->
  <!--   <button -->
  <!--     class="rounded px-2 m-2 text-white bg-purple-900" -->
  <!--     on:click={() => (firstNumber -= secondNumber)} -->
  <!--   > -->
  <!--     -= version -->
  <!--   </button> -->
  <!-- </div> -->

  <!-- <br /> -->
  <!-- compound assignment with augmented addition -->
  <!-- <br /> -->

  <!-- <br /> -->
  <!-- compound assignment with augmented addition -->
  <!-- <br /> -->
</div>

<div>
  <button
    class="rounded px-2 m-2 text-white bg-purple-900"
    on:click={() => firstNumber++}>increment by one</button
  >
  <button
    class="rounded px-2 m-2 text-white bg-purple-900"
    on:click={() => firstNumber--}>decrement by one</button
  >
</div>
