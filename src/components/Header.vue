<script>

</script>

<template lang="">
    <header>
        <nav class="container">
            <div class="branding">
                <img class="iconka" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.gh3B8Dci133ATtBdUQpjoAAAAA%26pid%3DApi&f=1&ipt=b63584b8d19f52d887a9f7cc0181642732d85bad1931d644a25e61863f86bebe&ipo=images" alt="icon">
                <h1>Vue Todos</h1>
                <ul class="nav-routes">
                    <router-link to="/">Home</router-link>
                    <router-link to="/about">About</router-link>
                </ul>
            </div>
        </nav> 
    </header>
</template>

<style lang="scss" scoped >
header {
    background-color: #f1f1f1;
    nav {
      display: flex;
      align-items: center;
      padding: 25px 16px;
      .branding {
        display: flex;
        align-items: center;
        gap: 8px;
        img {
          max-width: 50px;
        }
        h1 {
          font-size: 24px;
        }
      }
      .nav-routes {
        display: flex;
        flex: 1;
        justify-content: flex-end;
        gap: 12px;
        list-style: none;
        a {
          text-decoration: none;
          color: inherit;
        }
      }
    }
  }
</style>