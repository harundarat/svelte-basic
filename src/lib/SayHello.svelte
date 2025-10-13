<script>
  let person = $state({
    firstName: "",
    lastName: "",
  });

  const sayHello = () => {
    // @ts-ignore
    person.firstName = document.getElementById("firstName").value;
    // @ts-ignore
    person.lastName = document.getElementById("lastName").value;
  };
</script>

<input type="text" name="firstName" id="firstName" placeholder="First Name" />
<br />
<input type="text" name="lastName" id="lastName" placeholder="Last Name" />
<br />
<button onclick={sayHello}>Say Hello</button>

<h1>{person.firstName} {person.lastName}</h1>
