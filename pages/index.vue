<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">หน้าหลัก</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
           
            
            <b-button size="sm" class="my-2 my-sm-0" type="submit"
              >หมวดหมู่</b-button
            >
            <b-button size="sm" class="my-2 my-sm-0" type="submit"
              >todo</b-button
            >
          </b-nav-form>

         
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {};
</script>
