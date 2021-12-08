<h1> FaunaDB </h1>
<h4> Criar a collection subscription </h4>
<img align="center" alt="faunadb"  src="https://github.com/eugeniol2/assets/blob/ignewsAssets/faunadb.png" />
<h4> Criar a collection users </h4>
<img align="center" alt="faunadbuser"  src="https://github.com/eugeniol2/assets/blob/ignewsAssets/faunadbuser.png" />

<h2> Indexes </h2>

  ```js
  {
    name: "subscription_by_id",
    unique: false,
    serialized: true,
    source: "subscription",
    terms: [
      {
        field: data.id
      }
    ]
  }  
  {
    name: "subscription_by_status",
    unique: false,
    serialized: true,
    source: "subscription",
    terms: [
      {
        field: data.status
      }
    ]
  }  
  {
    name: "subscription_by_user_ref",
    unique: false,
    serialized: true,
    source: "subscription",
    terms: [
      {
        field: data.userId
      }
    ]
  }  
  {
    name: "user_by_email",
    unique: true,
    serialized: true,
    source: "users",
    terms: [
      {
        field: data.email
      }
    ]
  }
  {
    name: "user_by_stripe_customer_id",
    unique: false,
    serialized: true,
    source: "users",
    terms: [
      {
        field: data.stripe_customer_id
      }
    ]
  }
  ```
<h1> Stripe </h1>
<p> Criar projeto e criar um produto com nome e preço </p>

<div>
  <section>
    <h1> Prismic </h1>
    <h4> Após a criação do repositório no prismic é necessário clicar em "custom types" e adicionar um novo type seguinto os dados abaixo: </h4>
    <ul>
      <li>Name: post</li>
      <li>Type: repeatable</li>
    </ul>
    <h2> Estrutura do post </h2>
    <ul>
      <li>UID</li> 
      <li>Title</li> 
      <li>Content</li> 
    </ul>
  </section>  
</div>
