<script>
   import { Button } from "$components"
   import BookCover from "$assets/book_cover.png"
   import PhoneCover from "$assets/phone_cover.png"

   let { children } = $props()
</script>

<section class="hero">
   <div class="hero-showcase text-center bold hero-text">
      <h1 class="purple mb-s">MOVE TO</h1>
      <h1 class="purple mb-xs">SPAIN</h1>
      <h4 class="italic semi-bold">No need to make the same mistakes I made</h4>
      <img class="book-cover" src={BookCover} alt="" />
      <img class="phone-cover" src={PhoneCover} alt="" />
   </div>

   <div class="hero-text white text-center">
      {#if children}
         {@render children()}
      {:else}
         <h2>THIS EBOOK WILL</h2>
         <h2>SAVE YOU MONEY,</h2>
         <h2 CLASS="mb-m">TIME & NERVE</h2>
         <p class="light-grey mb-l">
            I moved to Spain seven years ago. The process was painful and
            difficult. I learned most things the hard way: finding a job,
            getting a visa, calculating my cost of living, choosing an
            apartment. That's why I wrote this e-book, to tell you how I did it.
            No bull, no stress.
         </p>
         <Button>Purchase an e-book for $10</Button>
      {/if}
   </div>
</section>

<style>
   .hero {
      display: flex;
      height: 100vh;
      overflow-y: hidden;
   }

   .hero-showcase {
      position: relative;
      width: 50%;
      padding: 100px 16px 0 16px;
      background: linear-gradient(
         135deg,
         #e2cbff,
         #e2cbff 25%,
         #deeaff 50%,
         #ece5ff 75%,
         #927bce
      );
   }

   .hero-text {
      padding: 100px 5%;
      width: 50%;
      background-color: black;
      font-size: 50px;
   }

   .book-cover {
      position: absolute;
      right: 2%;
      top: 22%;
      bottom: 0;
      width: 65%;
      transform: translateY(30%);
      overflow: hidden;
   }

   .phone-cover {
      position: absolute;
      width: 35%;
      bottom: 0;
      right: 52%;
      transform: translateY(25%);
   }
</style>
