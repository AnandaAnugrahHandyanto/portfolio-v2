<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Develop Applications with Alibaba Cloud Services',
          imageUrl: 'developaplication',
          status: 'By Alibaba Cloud.',
        },
        {
          id: 2,
          name: 'Learn Basic Web Programming HTML',
          imageUrl: 'html',
          status: 'By Alibaba Cloud x Codepolitan x Developer Handal.',
        },
        {
          id: 3,
          name: 'Learn Basic Web Programming CSS',
          imageUrl: 'css',
          status: 'By Alibaba Cloud x Codepolitan x Developer Handal.',
        },
        {
          id: 4,
          name: 'Learn Basic Web Programming Bootstrap CSS Framework',
          imageUrl: 'bootstrapcss',
          status: 'By Alibaba Cloud x Codepolitan x Developer Handal.',
        },
        {
          id: 5,
          name: 'Learn Basic Web Programming JavaScript',
          imageUrl: 'javascript',
          status: 'By Alibaba Cloud x Codepolitan x Developer Handal.',
        },
        {
          id: 6,
          name: 'Introduction to DevOps',
          imageUrl: 'devops',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 7,
          name: 'Introduction to Alibaba Cloud CLI',
          imageUrl: 'cloudcli',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 8,
          name: 'Introduction to ACK',
          imageUrl: 'ack',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 9,
          name: 'Introduction to Function Coumpute',
          imageUrl: 'compute',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 10,
          name: 'Introduction to ARMS',
          imageUrl: 'arms',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 11,
          name: 'Introduction to Alibaba Cloud ROS',
          imageUrl: 'ros',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 12,
          name: 'Introduction to Ansible',
          imageUrl: 'ansible',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 13,
          name: 'Introduction to GIT',
          imageUrl: 'git',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 14,
          name: 'Introduction to IaC',
          imageUrl: 'iac',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 15,
          name: 'Introduction to Jenkins',
          imageUrl: 'jenkins',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
        {
          id: 16,
          name: 'Introduction to Serverles Computing',
          imageUrl: 'serverlesscomputing',
          status: 'By Alibaba Cloud x Codepolitan.',
        },
      ]
    };
  }
}
</script>

<template>
  <div class="py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-10 fadein-bot title-section flex items-center justify-center flex-col">
          <h4>Certification</h4>
          <h4 class="text-base font-normal text-transparent bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300">
            Welcome to my certification gallery. Here, you can see the official recognitions I've received for my skills and knowledge in web development and related fields. Each certificate represents a milestone in my ongoing professional development
          </h4>
        </div>
      </header>
      <section>
        <div>
          <div class="grid grid-cols-1 gap-4 pb-32 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3 2xl:grid-cols-4 fade-zoom-in">
            <div v-for="item in items" :key="item.id">
              <div class="item-card flex flex-col items-center gap-2 rounded bg-[#1e1e1f] hover:bg-[#282828] border border-[#383838] rounded-xl text-amber-50 md:gap-3 px-5 py-5 lg:px-5 ">
                <div class="flex h-12 w-12 items-center justify-center p-0 h-full w-full lg:p-0 zoom-in">
                  <img alt="HTML" loading="lazy" decoding="async" data-nimg="1" class="drop-shadow-xl rounded rounded-xl" :src="'/certification/certification-' + item.imageUrl + '.png'">
                </div>
                <div class="w-full flex flex-col gap-2 items-center text-sm md:text-base lg:text-lg">
                  <div class="title-text font-medium text-secondary">{{ item.name }}</div>
                  <div class="w-full text-left text-[10px] text-[#c1c1c1] md:text-xs lg:text-sm">{{ item.status }}</div>
                  <div class="w-full mt-4 text-normal text-sm text-left text-amber-200">{{ item.tech }}</div>
                  <div class="w-full flex justify-end">
                    <div class="flex cursor-pointer items-end gap-2 text-primary">
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
body {
  overflow-x: hidden;
}

.item-card:hover {
  transition: transform 0.3s ease;
  transform: translateY(-8px);
}

svg:hover {
  stroke: #ffdb70;
}

@keyframes fadeZoomIn {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

/* Menggunakan animasi pada elemen yang diinginkan */
.fade-zoom-in {
  animation: fadeZoomIn 1s ease-in-out;
}

/* Responsive adjustments */
@media only screen and (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr !important;
  }
}
@media only screen and (min-width: 769px) and (max-width: 1024px) {
  .grid {
    grid-template-columns: repeat(2, 1fr) !important;
  }
}
@media only screen and (min-width: 1025px) and (max-width: 1440px) {
  .grid {
    grid-template-columns: repeat(3, 1fr) !important;
  }
}
@media only screen and (min-width: 1441px) {
  .grid {
    grid-template-columns: repeat(4, 1fr) !important;
  }
}
</style>
  