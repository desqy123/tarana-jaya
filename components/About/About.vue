<template>
  <section class="py-8 px-4 mt-10">
    <div class="flex flex-wrap justify-center lg:justify-between -mx-2">
      <div class="lg:w-2/5 px-2 flex lg:pr-16 mb-6 lg:mb-0">
        <img
          src="/img/logo-tjm.jpeg"
          alt=""
          style="height: 150px;"
          class="mx-auto"
        />
      </div>
      <div class="lg:w-3/5 mx-auto">
        <h2 class="text-4xl font-bold">{{ $t('about.title') }}</h2>
        <p class="text-gray-800 mt-3 text-justify">
          {{ $t('about.description') }}
        </p>
        <button
          class="bg-transparent hover:bg-purple-500 text-purple-700 font-semibold hover:text-white py-2 px-4 border border-purple-500 hover:border-transparent rounded mt-5"
          onclick="downloadAll(window.links)"
        >
          Download Company Profile

          <!-- <a
            href="/img/page/about/Tarana Jaya Mandiri Company Profile.pdf"
            download
            >Download Company Profile</a
          > -->

          <!-- SCRIPT MULTIPLE DOWNLOADS -->
          <script>
            var links = [
              '/img/page/about/SURAT AKTA NOTARIS ,CV TJM.pdf',
              '/img/page/about/SURAT IMB ,CV.TJM.pdf',
              '/img/page/about/SURAT KOMANDITER CV ,TJM.pdf',
              '/img/page/about/SURAT NPWP ,CV.TJM.pdf',
              '/img/page/about/SURAT SITU ,CV.TJM.pdf',
              '/img/page/about/SURAT SIUP ,CV.TJM.pdf',
              '/img/page/about/Tarana Jaya Mandiri Company Profile.pdf',
            ]

            function downloadAll(urls) {
              var link = document.createElement('a')

              link.setAttribute('download', null)
              link.style.display = 'none'

              document.body.appendChild(link)

              for (var i = 0; i < urls.length; i++) {
                link.setAttribute('href', urls[i])
                link.click()
              }

              document.body.removeChild(link)
            }
          </script>
        </button>
      </div>
    </div>
  </section>
</template>
