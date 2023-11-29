<template>
  <div>
    <nav class="bg-white border-b">
      <div class="mx-auto">
        <div class="flex h-16 px-5">
          <div class="flex">
            <div class="flex flex-shrink-0 items-center font-bold text-xl">
              FY21 - Recommended Operating Budget
            </div>
          </div>
          <div
            class="flex flex-1 items-center justify-center px-2 lg:ml-6 lg:justify-end"
          >
            <div class="w-full max-w-lg lg:max-w-xs">
              <label for="search" class="sr-only">Search</label>
              <div class="relative">
                <div
                  class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3"
                >
                  <svg
                    class="h-5 w-5 text-gray-400"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                    aria-hidden="true"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M9 3.5a5.5 5.5 0 100 11 5.5 5.5 0 000-11zM2 9a7 7 0 1112.452 4.391l3.328 3.329a.75.75 0 11-1.06 1.06l-3.329-3.328A7 7 0 012 9z"
                      clip-rule="evenodd"
                    />
                  </svg>
                </div>
                <input
                  id="search"
                  name="search"
                  class="block w-full rounded-md border-0 bg-white py-1.5 pl-10 pr-3 text-gray-900 ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                  placeholder="Search Proposal..."
                  type="search"
                />
              </div>
            </div>
          </div>
          <div class="hidden lg:ml-4 lg:flex lg:items-center">
            <button
              type="button"
              class="rounded-md bg-white px-3 py-2 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50"
            >
              Export
            </button>

            <!-- Profile dropdown -->
            <div class="relative ml-4 flex-shrink-0">
              <div>
                <button
                  type="button"
                  class="rounded-md bg-black px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-gray-800 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                >
                  Create Proposal
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </nav>

    <!-- For navigation -->
    <div class="bg-white border-b px-5 py-2 text-sm h-10 flex items-center">
      <span class="text-gray-600">Budget</span>&nbsp;/&nbsp;<span class="font-semibold">FY21 - Recommended Operating Budget</span>
    </div>
  </div>
</template>
