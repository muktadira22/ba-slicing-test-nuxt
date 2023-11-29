<template>
  <div>
    <div class="mt-8 flow-root">
      <div class="-mx-4 -my-2 overflow-x-auto sm:-mx-6 lg:-mx-8">
        <div class="inline-block min-w-full py-2 align-middle sm:px-6 lg:px-8">
          <div
            class="overflow-hidden shadow ring-1 ring-black ring-opacity-5 sm:rounded-lg"
          >
            <table class="min-w-full divide-y divide-gray-300">
              <thead class="bg-gray-50">
                <tr>
                  <th
                    scope="col"
                    class="py-3.5 pl-4 pr-3 text-left text-sm font-semibold text-gray-900 sm:pl-6"
                  >
                    Proposals
                  </th>
                  <th
                    scope="col"
                    class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900"
                  >
                    Status
                  </th>
                  <th
                    scope="col"
                    class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900"
                  >
                    Creates By
                  </th>
                  <th
                    scope="col"
                    class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900"
                  >
                    Expense
                  </th>
                  <th
                    scope="col"
                    class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900"
                  >
                    Revenue
                  </th>
                  <th
                    scope="col"
                    class="px-3 py-3.5 text-left text-sm font-semibold text-gray-900"
                  >
                    Surplus/-Deficit
                  </th>
                  <th scope="col" class="relative py-3.5 pl-3 pr-4 sm:pr-6">
                    <span class="sr-only"></span>
                  </th>
                </tr>
              </thead>
              <tbody class="divide-y divide-gray-200 bg-white">
                <tr v-for="(item, key) in items" :key="key">
                  <td
                    scope="col"
                    class="py-2 pl-4 pr-3 text-sm text-gray-900 sm:pl-6"
                  >
                    <span class="font-medium">{{ item.proposal }}</span
                    ><br />
                    <span class="font-light">{{ item.sub_proposal }}</span>
                  </td>
                  <td scope="col" class="px-3 py-3.5 text-sm text-gray-900">
                    <span
                      class="text-white py-1 px-2 rounded-md"
                      :style="{ 'background-color': item.status_color }"
                      >{{ item.status }}</span
                    >
                  </td>
                  <td>
                    <div class="flex text-left items-center space-x-2">
                      <div
                        class="bg-green-500 text-white py-1.5 px-2 rounded-md text-sm"
                      >
                        {{ item.created_by_init }}
                      </div>
                      <div>
                        <span class="font-medium">{{ item.created_by }}</span>
                        <br />
                        <span class="font-light"
                          >{{ item.day }}&nbsp;days ago</span
                        >
                      </div>
                    </div>
                  </td>
                  <td class="text-right">
                    <span class="font-medium">${{ item.expanse }}</span
                    ><br />
                    <span class="font-light text-sm text-red-500"
                      >{{ item.expanse_percentage }}%</span
                    >
                  </td>
                  <td class="text-right">
                    <span class="font-medium">${{ item.revenue }}</span
                    ><br />
                    <span class="font-light text-sm text-green-500"
                      >{{ item.revenue_percentage }}%</span
                    >
                  </td>
                  <td class="text-right">
                    <span class="font-medium">${{ item.surplus }}</span
                    ><br />
                    <span class="font-light text-sm text-green-500"
                      >{{ item.surplus_percentage }}%</span
                    >
                  </td>
                  <td class="py-4 px-5 grid justify-items-end">
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
                        d="M20.25 7.5l-.625 10.632a2.25 2.25 0 01-2.247 2.118H6.622a2.25 2.25 0 01-2.247-2.118L3.75 7.5m6 4.125l2.25 2.25m0 0l2.25 2.25M12 13.875l2.25-2.25M12 13.875l-2.25 2.25M3.375 7.5h17.25c.621 0 1.125-.504 1.125-1.125v-1.5c0-.621-.504-1.125-1.125-1.125H3.375c-.621 0-1.125.504-1.125 1.125v1.5c0 .621.504 1.125 1.125 1.125z"
                      />
                    </svg>
                  </td>
                </tr>

                <!-- <tr>
                  <td
                    class="whitespace-nowrap py-4 pl-4 pr-3 text-sm font-medium text-gray-900 sm:pl-6"
                  >
                    Lindsay Walton
                  </td>
                  <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
                    Front-end Developer
                  </td>
                  <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
                    lindsay.walton@example.com
                  </td>
                  <td class="whitespace-nowrap px-3 py-4 text-sm text-gray-500">
                    Member
                  </td>
                  <td
                    class="relative whitespace-nowrap py-4 pl-3 pr-4 text-right text-sm font-medium sm:pr-6"
                  >
                    <a href="#" class="text-indigo-600 hover:text-indigo-900"
                      >Edit<span class="sr-only">, Lindsay Walton</span></a
                    >
                  </td>
                </tr> -->

                <!-- More people... -->
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>

    <!-- Pagination -->

    <div
      class="flex items-center justify-between border-t border-gray-200 bg-white px-4 py-3 sm:px-6"
    >
      <div class="flex flex-1 justify-between sm:hidden">
        <a
          href="#"
          class="relative inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50"
          >Previous</a
        >
        <a
          href="#"
          class="relative ml-3 inline-flex items-center rounded-md border border-gray-300 bg-white px-4 py-2 text-sm font-medium text-gray-700 hover:bg-gray-50"
          >Next</a
        >
      </div>
      <div class="hidden sm:flex sm:flex-1 sm:items-center sm:justify-between">
        <div>
          <p class="text-sm text-gray-700">
            Showing
            <span class="font-medium">1</span>
            to
            <span class="font-medium">10</span>
            of
            <span class="font-medium">97</span>
            results
          </p>
        </div>
        <div>
          <nav
            class="isolate inline-flex -space-x-px rounded-md shadow-sm"
            aria-label="Pagination"
          >
            <a
              href="#"
              class="mr-2 relative inline-flex items-center rounded-md px-2 py-2 text-gray-400 ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:z-20 focus:outline-offset-0"
            >
              <span class="sr-only">Previous</span>
              <svg
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="currentColor"
                aria-hidden="true"
              >
                <path
                  fill-rule="evenodd"
                  d="M12.79 5.23a.75.75 0 01-.02 1.06L8.832 10l3.938 3.71a.75.75 0 11-1.04 1.08l-4.5-4.25a.75.75 0 010-1.08l4.5-4.25a.75.75 0 011.06.02z"
                  clip-rule="evenodd"
                />
              </svg>
            </a>

            <a
              href="#"
              class="relative inline-flex items-center rounded-md px-2 py-2 text-white ring-1 ring-inset ring-black bg-black hover:bg-gray-50 focus:z-20 focus:outline-offset-0"
            >
              <span class="sr-only">Next</span>
              <svg
                class="h-5 w-5"
                viewBox="0 0 20 20"
                fill="currentColor"
                aria-hidden="true"
              >
                <path
                  fill-rule="evenodd"
                  d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z"
                  clip-rule="evenodd"
                />
              </svg>
            </a>
          </nav>
        </div>
      </div>
    </div>
    <!-- Ending Pagination -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          proposal: "Administration Department",
          sub_proposal: "The Administration Department..",
          status: "In Review",
          status_color: "#658CD9",
          created_by: "Ralph Edwards",
          created_by_init: "RE",
          day: 16,
          expanse: 4502343,
          expanse_percentage: 9.96,
          revenue: 4502343,
          revenue_percentage: 9.96,
          surplus: 4502343,
          surplus_percentage: 9.96,
        },
      ],
    };
  },
};
</script>
