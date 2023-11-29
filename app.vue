<template>
  <div>
    <AppLayout>
      <!-- Wrapper -->
      <div class="flex h-[calc(100vh-104px)]">
        <div class="w-1/5 border-r">
          <!-- Title -->
          <div class="flex font-semibold h-12 border-b px-3 items-center">
            Budget Summary
          </div>
          <div class="px-3 space-y-2 border-b py-4 mb-4">
            <div class="font-medium mb-4">Balance</div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Based Revenues</span>
              <span class="">$42.059.705</span>
            </div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Adjustments</span>
              <span class="text-green-500">$0</span>
            </div>
            <div class="flex justify-between text-sm font-medium pb-2">
              <span>Revenues</span>
              <span>$42.059.705</span>
            </div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Base Expanses</span>
              <span class="text-">$200.631.271</span>
            </div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Adjustments</span>
              <span class="text-red-500">+$4.157.674</span>
            </div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Position Requests</span>
              <span class="text-red-500">$0</span>
            </div>
            <div class="flex justify-between text-sm font-medium pb-5 border-b">
              <span>Expanses</span>
              <span>$204.788.945</span>
            </div>
            <div class="flex justify-between text-sm">
              <span class="text-gray-600">Deficit</span>
              <span class="text-red-500">$162.729.240</span>
            </div>
          </div>
          <!-- Phase -->
          <div class="mx-3 border-b pb-4">
            <div class="flex justify-between font-medium mb-5">
              <span>Phase</span>
              <span class="underline">See All</span>
            </div>
            <div class="space-y-2">
              <div class="flex items-center space-x-2">
                <div class="rounded-full bg-black p-1 text-white">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke-width="1.5"
                    stroke="currentColor"
                    class="w-5 h-5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M4.5 12.75l6 6 9-13.5"
                    />
                  </svg>
                </div>
                <div>City Manager Review</div>
              </div>
              <div class="flex items-center space-x-2">
                <div
                  class="w-7 h-7 rounded-full border inline-flex items-center justify-center bg-white"
                >
                  4
                </div>
                <div>Board of Finance Review</div>
              </div>
              <div class="flex items-center space-x-2">
                <div
                  class="w-7 h-7 rounded-full border inline-flex items-center justify-center bg-white"
                >
                  5
                </div>
                <div>Final</div>
              </div>
            </div>
          </div>
          <!-- End Phase -->
          <div class="grid justify-items-center p-4">
            <button
              type="button"
              class="rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50"
            >
              Move to next phase
            </button>
          </div>
        </div>
        <div class="w-4/5">
          <!-- Tabs Navigate -->
          <div class="flex border-b">
            <div
              class="flex font-semibold h-12 border-r px-3 items-center bg-gray-200"
            >
              Proposals
            </div>
            <div class="flex font-semibold h-12 border-r px-3 items-center">
              Line Items
            </div>
          </div>
          <!-- End of Tabs Navigate -->

          <!-- Main Content -->
          <div class="p-4">
            <div class="border border-gray-200 bg-white rounded-md">
              <div class="border-b px-4 py-3">
                <div
                  class="-ml-4 -mt-2 flex flex-wrap items-center justify-between sm:flex-nowrap"
                >
                  <div class="ml-4 mt-2">
                    <div class="flex items-center space-x-2">
                      <svg
                        xmlns="http://www.w3.org/2000/svg"
                        fill="none"
                        viewBox="0 0 24 24"
                        stroke-width="1.5"
                        stroke="currentColor"
                        class="w-6 h-6"
                      >
                        <path
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          d="M4.5 15.75l7.5-7.5 7.5 7.5"
                        />
                      </svg>

                      <h3
                        class="text-base font-semibold leading-6 text-gray-900"
                      >
                        Visualization
                      </h3>
                      <button
                        type="button"
                        class="rounded-md bg-black px-2.5 py-1.5 text-sm font-semibold text-white shadow-sm hover:bg-gray-800 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                      >
                        Create Proposal
                      </button>
                      <div class="text-sm bg-gray-200 py-1 px-2 rounded-md">
                        Showing
                        <span class="font-semibold">Expanses</span> broken down
                        by <span class="font-semibold">Departments</span>
                      </div>
                    </div>
                  </div>
                  <div class="ml-4 mt-2 flex flex-shrink-0 items-center">
                    <label
                      class="inline-block pl-[0.15rem] hover:cursor-pointer mr-2 font-semibold"
                      for="flexSwitchCheckDefault"
                      >Legend</label
                    >
                    <input
                      class="mt-[0.3rem] h-3.5 w-8 appearance-none rounded-[0.4375rem] bg-neutral-300 before:pointer-events-none before:absolute before:h-3.5 before:w-3.5 before:rounded-full before:bg-transparent before:content-[''] after:absolute after:z-[2] after:-mt-[0.1875rem] after:h-5 after:w-5 after:rounded-full after:border-none after:bg-neutral-100 after:shadow-[0_0px_3px_0_rgb(0_0_0_/_7%),_0_2px_2px_0_rgb(0_0_0_/_4%)] after:transition-[background-color_0.2s,transform_0.2s] after:content-[''] checked:bg-primary checked:after:absolute checked:after:z-[2] checked:after:-mt-[3px] checked:after:ml-[1.0625rem] checked:after:h-5 checked:after:w-5 checked:after:rounded-full checked:after:border-none checked:after:bg-primary checked:after:shadow-[0_3px_1px_-2px_rgba(0,0,0,0.2),_0_2px_2px_0_rgba(0,0,0,0.14),_0_1px_5px_0_rgba(0,0,0,0.12)] checked:after:transition-[background-color_0.2s,transform_0.2s] checked:after:content-[''] hover:cursor-pointer focus:outline-none focus:ring-0 focus:before:scale-100 focus:before:opacity-[0.12] focus:before:shadow-[3px_-1px_0px_13px_rgba(0,0,0,0.6)] focus:before:transition-[box-shadow_0.2s,transform_0.2s] focus:after:absolute focus:after:z-[1] focus:after:block focus:after:h-5 focus:after:w-5 focus:after:rounded-full focus:after:content-[''] checked:focus:border-primary checked:focus:bg-primary checked:focus:before:ml-[1.0625rem] checked:focus:before:scale-100 checked:focus:before:shadow-[3px_-1px_0px_13px_#3b71ca] checked:focus:before:transition-[box-shadow_0.2s,transform_0.2s] dark:bg-neutral-600 dark:after:bg-neutral-400 dark:checked:bg-primary dark:checked:after:bg-primary dark:focus:before:shadow-[3px_-1px_0px_13px_rgba(255,255,255,0.4)] dark:checked:focus:before:shadow-[3px_-1px_0px_13px_#3b71ca]"
                      type="checkbox"
                      role="switch"
                      id="flexSwitchCheckDefault"
                    />
                  </div>
                </div>
              </div>
              <div class="px-4 py-5 h-96 w-auto grid justify-items-center">
                <BarChart />
              </div>
            </div>

            <Table />
          </div>

          <!-- End of Main Content -->
        </div>
      </div>
    </AppLayout>
  </div>
</template>
