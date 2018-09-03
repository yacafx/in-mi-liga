<template>

	<b-container>
		<b-row>
      <b-col>
          <b-button variant="success" size="lg">
            Mi botón
          </b-button>
        </b-col>
      <b-col>
        <b-button :pressed="false" variant="warning">
          Mi botón
        </b-button>
      </b-col>
      <b-col>
        <b-button variant="primary"  size="sm">
          Mi botón
        </b-button>
      </b-col>
    </b-row>
    <!--
		<b-row>
      <b-col>Grid System</b-col>
    </b-row>
    -->
	</b-container>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
  //  msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
/*
ul {
  list-style-type: none;
  padding: 0;
}*/
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
