<script setup lang="ts"></script>

<template>
  <div class="mt-20 py-12 items-center h-[150px] bg-gray-900 font-poppins">
    <div class="flex justify-between flex-wrap">
      <div>
        <div class="mx-32 text-white text-base font-semibold leading-[30px]">
          Join our newsletter
        </div>
        <div class="mx-32 text-gray-200 text-sm font-normal leading-normal">
          Join over 4,000+ startups already growing with Morpheme.
        </div>
      </div>
      <div class="flex-row">
        <div class="flex justify-evenly mr-32 gap-3">
          <form>
            <input
              placeholder="Enter your email"
              @keydown.enter.prevent=""
              class="h-8 w-52 bg-white px-2 rounded-md text-gray-500 text-xs font-normal leading-tight"
            />
          </form>
          <button
            class="h-8 w-20 px-2 rounded-md bg-sky-600 hover:bg-sky-700 pt-0.5 text-center text-white text-xs font-normal leading-tight"
          >
            Subscribe
          </button>
        </div>
        <button class="mr-32 my-2 text-white">
          <img src="~/assets/icons/Info.svg" />
        </button>
      </div>
    </div>
  </div>
  <div class="py-12 items-center h-[420px] bg-slate-800 font-poppins">
    <div class="flex justify-between">
      <div>
        <div class="flex flex-start mx-32 gap-x-2">
          <img src="~/assets/icons/Content.svg" width="30" />
          <img src="~/assets/images/Gits2.png" width="110" />
        </div>
        <div
          class="ml-32 mt-6 w-64 text-gray-200 text-sm font-normal leading-normal"
        >
          Design amazing digital experiences that create more happy in the
          world.
        </div>
      </div>
      <div class="text-white ml-20 mr-44 mb-8">
        <div
          class="grow shrink basis-0 h-60 justify-start items-start gap-16 flex"
        >
          <div
            class="grow shrink basis-0 flex-col justify-start items-start gap-4 inline-flex"
          >
            <div
              class="self-stretch text-gray-300 text-sm font-medium leading-tight"
            >
              Product
            </div>
            <div
              class="self-stretch h-[204px] w-[85px] flex-col justify-start items-start gap-3 flex"
            >
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Overview</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Features</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Solutions</NuxtLink>
                  </div>
                </div>
                <div
                  class="px-2 py-0.5 bg-white bg-opacity-10 rounded-2xl border border-white border-opacity-30 justify-start items-center flex"
                >
                  <div
                    class="text-center text-white text-xs font-sm leading-[15px]"
                  >
                    <NuxtLink to="/">New</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Tutorials</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Pricing</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Releases</NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            class="grow shrink basis-0 flex-col justify-start items-start gap-4 inline-flex"
          >
            <div
              class="self-stretch text-gray-300 text-sm font-medium leading-tight"
            >
              Company
            </div>
            <div
              class="self-stretch h-[204px] w-[74px] flex-col justify-start items-start gap-3 flex"
            >
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">About us</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Careers</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Press</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">News</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Media kit</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Contact</NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            class="grow shrink basis-0 flex-col justify-start items-start gap-4 inline-flex -mr-2"
          >
            <div
              class="self-stretch text-gray-300 text-sm font-medium leading-tight"
            >
              Resources
            </div>
            <div
              class="self-stretch h-[204px] w-[93px] flex-col justify-start items-start gap-3 flex"
            >
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Blog</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Newsletter</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Events</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Help centre</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Tutorials</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Support</NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            class="grow shrink basis-0 flex-col justify-start items-start gap-4 inline-flex"
          >
            <div
              class="self-stretch text-gray-300 text-sm font-medium leading-tight"
            >
              Social
            </div>
            <div
              class="self-stretch h-[204px] w-[65px] flex-col justify-start items-start gap-3 flex"
            >
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Twitter</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">LinkedIn</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Facebook</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">GitHub</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">AngelList</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Dribbble</NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div
            class="grow shrink basis-0 flex-col justify-start items-start gap-4 inline-flex"
          >
            <div
              class="self-stretch text-gray-300 text-sm font-medium leading-tight"
            >
              Legal
            </div>
            <div
              class="self-stretch h-[204px] w-[65px] flex-col justify-start items-start gap-3 flex"
            >
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Terms</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Privacy</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Cookies</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Licenses</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Settings</NuxtLink>
                  </div>
                </div>
              </div>
              <div class="justify-start items-center gap-2 inline-flex">
                <div class="justify-center items-center gap-2 flex">
                  <div
                    class="text-gray-200 text-base font-medium leading-normal"
                  >
                    <NuxtLink to="/">Contact</NuxtLink>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="mx-32 pt-6 flex-col justify-start items-start gap-8 flex">
      <div
        class="self-stretch pt-6 border-t border-slate-600 justify-start items-center gap-8 inline-flex"
      >
        <div
          class="grow shrink basis-0 text-gray-500 text-base font-normal leading-normal"
        >
          © 2077 Morpheme UI. All rights reserved.
        </div>
        <div class="justify-start items-center gap-6 flex">
          <div class="w-6 h-6 relative">
            <NuxtLink to="/"><img src="~/assets/icons/Twitter.svg" /></NuxtLink>
          </div>
          <div class="w-6 h-6 justify-center items-center flex">
            <NuxtLink to="/"
              ><img src="~/assets/icons/Linkedin.svg"
            /></NuxtLink>
          </div>
          <div class="w-6 h-6 relative">
            <NuxtLink to="/"
              ><img src="~/assets/icons/Facebook.svg"
            /></NuxtLink>
          </div>
          <div class="w-6 h-6 relative">
            <NuxtLink to="/"><img src="~/assets/icons/Github.svg" /></NuxtLink>
          </div>
          <div class="w-6 h-6 relative">
            <NuxtLink to="/"><img src="~/assets/icons/Peace.svg" /></NuxtLink>
          </div>
          <div class="w-6 h-6 relative">
            <NuxtLink to="/"><img src="~/assets/icons/Ball.svg" /></NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
