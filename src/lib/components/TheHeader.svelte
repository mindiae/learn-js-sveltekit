<script>
  import NavLink from '$lib/components/NavLink.svelte';
  import ResponsiveNavLink from '$lib/components/ResponsiveNavLink.svelte';
  import ApplicationMark from '$lib/components/ApplicationMark.svelte';
  import { page } from '$app/stores';

  const navItems = [
    {
      title: 'ძირითადი',
      path: '/'
    },
    {
      title: 'კონტაქტი',
      path: '/contact/'
    }
  ];
  let showingNavigationDropdown = false;
</script>

<header>
  <nav class="bg-white border-b border-gray-100">
    <!-- Primary Navigation Menu -->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="shrink-0 flex items-center">
          <a href="/">
            <ApplicationMark />
          </a>
        </div>
        <div class="flex">
          <!-- Navigation Links -->
          <div
            class="hidden space-x-8 sm:-my-px sm:ml-10 sm:flex"
          >
            {#each navItems as navItem (navItem.title)}
              <NavLink
                href={navItem.path}
                active={navItem.path == $page.url.pathname}
              >
                {navItem.title}
              </NavLink>
            {/each}
          </div>

          <!-- Hamburger -->
          <div class="-mr-2 flex items-center sm:hidden">
            <button
              class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:bg-gray-100 focus:text-gray-500 transition"
              on:click={() =>
                (showingNavigationDropdown =
                  !showingNavigationDropdown)}
            >
              <svg
                class="h-6 w-6"
                stroke="currentColor"
                fill="none"
                viewBox="0 0 24 24"
              >
                <path
                  class={showingNavigationDropdown
                    ? 'hidden'
                    : 'inline-flex'}
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
                <path
                  class={!showingNavigationDropdown
                    ? 'hidden'
                    : 'inline-flex'}
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Responsive Navigation Menu -->
      <div
        class="sm:hidden {showingNavigationDropdown
          ? 'block'
          : 'hidden'}"
      >
        <div class="pt-2 pb-3 space-y-1">
          {#each navItems as navItem (navItem.title)}
            <ResponsiveNavLink
              href={navItem.path}
              active={navItem.path == $page.url.pathname}
            >
              {navItem.title}
            </ResponsiveNavLink>
          {/each}
        </div>
      </div>
    </div>
  </nav>
</header>
