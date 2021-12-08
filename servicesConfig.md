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
