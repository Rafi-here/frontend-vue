<script setup>
import { IconKacamataPembesar } from '@/components/icons'
import { g1, g2, g3, g4, g5, logo1, logo2, logo3, logo4, logo5, human, human2, human3, petik, category,
  shop, confetti, inbox, medal, gallery1, gallery2, kursi} from '@/assets/image'
import { CardComponent } from '@/components'
import { HeadingSubsection } from '@/components'
import FurnitureReview from '@/components/FurnitureReview.vue'



const images = [g1, g2, g3, g4, g1, g2]
const logos = [logo1, logo2, logo3, logo4, logo5]

const barang = [
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g1,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g2,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g3,
  },
  {
    title: 'LifeStyle Green Chair',
    harga: 105.0,
    gambar: g4,
  },
  {
    title: 'LifeStyle Cupboard',
    harga: 185.0,
    gambar: g5,
  },
  {
    title: 'LifeStyle Desk',
    harga: 205.0,
    gambar: g1,
  },
]
</script>

<template>
  <section id="sectionHero" class="space-y-20">
    <div class="space-y-[27px]">
      <h1 class="text-7xl text-black font-medium text-center mt-60 mx-60">
        Transform your space, Elevate your style.
      </h1>
      <h2 class="text-xl text-center mx-60">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex error veritatis tempore quae
        magni in temporibus, maiores vel. Nobis, dolore quod. Excepturi, molestiae aliquam vel
        explicabo laborum autem velit nesciunt!
      </h2>
    </div>

    <div class="flex justify-center w-full">
      <div class="flex justify-center w-[667px] py-4 pr-4 pl-6 bg-gray-200">
        <IconKacamataPembesar class="m-4" />
        <input
          class="bg-gray-200 outline-none border border-gray-200 w-full"
          placeholder="Search your property"
        />
        <button class="bg-orange-600 p-3 text-white">Search</button>
      </div>
    </div>

    <!-- gambar -->
    <div class="flex space-x-10">
      <div class="overflow-x-auto" v-for="gambar in images">
        <img :src="gambar" alt="gambar1" class="object-cover h-80 w-80" />
      </div>
    </div>

    <div class="flex justify-between">
      <div class="mx-4" v-for="logo in logos">
        <img :src="logo" alt="logo" class="object-cover" />
      </div>
    </div>
  </section>

  <div>
  <HeadingSubsection />
  </div>

  <section id="card" class="my-20 w-full">
    <div class="w-full grid grid-cols-3 gap-20">
      <CardComponent
        v-for="product in barang"
        :key="index"
        :title="product.title"
        :harga="product.harga"
        :gambar="product.gambar"
      />
    </div>
  </section>

  <div class="testimonial bg-gray-200 py-10 mb-20">
    <div class="frame text-center mb-12 space-y-2">
      <div class="div-wrapper">
        <div class="text-m font-bold text-orange-600 bg-gray-300 p-2 mx-auto max-w-60 mt-10 rounded">Testimonial Section</div>
      </div>

      <div class="div font-extrabold text-4xl">What Our Customer Say</div>

      <p class="p">
        Lorem Ipsum is simply dummy text of the printing and typesetting
        industry.
      </p>
    </div>

    <div class="frame-2 grid grid-cols-1 md:grid-cols-3 gap-6 px-4 md:px-10">
      <div class="frame-3 bg-gray-300 rounded-lg p-6">
        <img :src="petik" class="img mb-10" alt="kutip" />

        <p class="text-wrapper-2">
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Pariatur natus aliquid minima quidem, culpa earum asperiores tempore recusandae? 
          Aperiam distinctio ducimus eveniet maxime, in porro eum odio enim rem quaerat?
        </p>

        <div class="group mt-10">
          <div class="frame-4 flex items-center gap-3">
            <img class="mask-group rounded-4xl" alt="Mask group" :src="human" />

            <div class="frame-5">
              <div class="text-wrapper-3">Johny Assloy</div>
            </div>

             <div class="flex gap-1 text-m">
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star text-gray-400"></i>
            </div>

          </div>
        </div>
      </div>

      <div class="frame-7 bg-gray-300 rounded-lg p-6">
        <img :src="petik" class="img mb-10" alt="kutip"/>

        <p class="text-wrapper-2">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. 
          Perferendis voluptatum pariatur dolorum, veritatis hic, velit
          expedita recusandae excepturi optio ipsum, eum molestias distinctio assumenda. 
          Illo laboriosam explicabo numquam labore quam.
        </p>

        <div class="group mt-10">
          <div class="frame-4 flex items-center gap-3">
            <img :src="human3" class="mask-group-2 rounded-4xl" alt="Mask group" />

            <div class="frame-5">
              <div class="text-wrapper-3"></div>
            </div>

             <div class="flex gap-1 text-m">
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
            </div>
          </div>

        </div>
      </div>

      <div class="frame-7 bg-gray-300 rounded-lg p-6">
        <img :src="petik" class="img mb-10" alt="kutip" />

        <p class="text-wrapper-2 mt-10">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facere aperiam nulla 
          nesciunt odit est magni cupiditate. Molestias pariatur repellat veritatis dolore 
          aspernatur fuga cupiditate ab, distinctio adipisci minima aut tenetur?
        </p>

        <div class="group mt-10">
          <div class="frame-4 flex items-center gap-3">
            <img :src="human2" class="mask-group-2" alt="Mask group"/>

            <div class="frame-5">
              <div class="text-wrapper-3">Sarah H</div>
            </div>

            <div class="flex gap-1 text-m">
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star" style="color: #F3C623;"></i>
              <i class="fas fa-star text-gray-400"></i>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>

   <div id="gallery" class="category w-full flex justify-center items-center my-10 mb-10">
    <div class="flex space-x-10">
      <img :src="category" alt="kursi" class="object-cover h-40 w-auto" />
    </div>
   </div>

   <div>
    <div class="frame text-center mb-12 space-y-2">
      <div class="div-wrapper">
        <div class="text-m font-bold text-orange-600 bg-gray-300 p-2 mx-auto max-w-60 mt-10 rounded">Testimonial Section</div>
      </div>

      <div class="div font-bold text-4xl">Our Furniture gallery</div>

      <p class="p font-normal text-gray-500 max-w-xl mx-auto">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Similique ducimus, possimus soluta quibusdam fugiat,
        magnam fuga quos odit consequuntur totam, cumque dolorum qui autem? Eveniet at non ipsum voluptas fuga.
      </p>
    </div>

     <div class="frame flex gap-3 justify-center items-center mb-10">
    <div class="div flex gap-2 border-1 border-blue-400 hover:border-blue-600 rounded-full w-20 h-10 px-2 items-center">
      <img
        class="img"
        alt="shop"
        :src="shop"
      />
      <div class="text-wrapper text-blue-900 ">All</div>
    </div>
    <div class="div-2 flex gap-2 border-1 border-gray-400 hover:border-blue-600 rounded-4xl w-40 h-10 px-2 items-center">
      <img
        class="img"
        alt="medal"
        :src="medal"
      />
      <div class="text-wrapper-2">Best Sellers</div>
    </div>
    <div class="div-2 flex gap-2 border-1 border-gray-400 hover:border-blue-600 rounded-4xl w-25 h-10 px-2 items-center">
      <img
        class="img"
        alt="confetti"
        :src="confetti"
      />
      <div class="text-wrapper-2">New</div>
    </div>
    <div class="div-2 flex gap-2 border-1 border-gray-400 hover:border-blue-600  rounded-4xl w-40 h-10 px-2 items-center">
      <img
        class="img"
        alt="inbox"
        :src="inbox"
      />
      <div class="text-wrapper-2">Up Coming</div>
    </div>
  </div>

    <div class="gallery flex flex-col gap-4 md:px-10 mb-20">
      <img :src="gallery1" alt="gallery1" class="object-cover h-auto w-full" />
      <img :src="gallery2" alt="gallery2" class="object-cover h-auto w-full" />
    </div>
   </div>

  <FurnitureReview :human="human" :kursi="kursi" />

</template>
