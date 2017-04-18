# How I learn graphql

I am very interested in graphql's approach to provide a thin layer between client and server and how easy of accessing the data from server and giving out the data to client. I have been reading and learning for a while and below are resouces that I think is very helpful in learning this relative new technology which I believe that it will become one the the player in API world very soon.

- [Awesome way to learn graphql](https://learngraphql.com/)
  - The same provider of another great tutorial of learning meteor. Very great starting point.
- [Graphql explained from former Apollo engineer.](https://dev-blog.apollodata.com/graphql-explained-5844742f195e)
  - One of the choice to keep going apart from the offical graphql doc
- [Former Apollo engineer teaching how to build Graphql servers](https://dev-blog.apollodata.com/how-to-build-graphql-servers-87587591ded5)
  - Build one graphql server yourself!
- [Full-stack grapnel + react tutorial](https://dev-blog.apollodata.com/full-stack-react-graphql-tutorial-582ac8d24e3b)
  - connection the dots, client <-> server
- [Graphql RFC specification](https://facebook.github.io/graphql/#sec-Overview)
  - Dive deeper

Sheatsheet
- [Graph Short Hand cheatsheet](https://raw.githubusercontent.com/sogko/graphql-shorthand-notation-cheat-sheet/master/graphql-shorthand-notation-cheat-sheet.png)

Video
- [Graphql At Facebook](https://dev-blog.apollodata.com/graphql-at-facebook-by-dan-schafer-38d65ef075af)
  - It is kind of a summary of a talk of How Facebook organise their Graphql code, especially how to handle business logic and permissions from Facebook. It is a summary but very important to know. It is just GOLD!
- [GitHub engineer announcing their graphql API](https://www.youtube.com/watch?v=wPPFhcqGcvk)
  - github has provided a graphql API in production that every one can try building app with it

Npm Package
- [Ths official graphql repo](http://facebook.github.io/graphql/)
- [Corated list of learning material or packages](https://github.com/chentsulin/awesome-graphql)
  - More materials, learnign, examples, etc.
- [Spawn a express server with grahpql api](https://github.com/graphql/express-graphql)
- [A promise version of mongodb](https://github.com/gordonmleigh/promised-mongo)

Schema examples
- https://github.com/kadirahq/graphql-blog-schema/blob/master/src/schema.js
- https://github.com/graphql/graphql-js/blob/master/src/__tests__/starWarsSchema.js
  - Must clone and try out the example from facebook and also how to test your schema.

Graphcool example app
- https://github.com/graphcool-examples
  - Graphcool is a serverless graphql backend, really good for building fast App, learn graphql by building mobile app using ReactNative, sounds great right?

Key Notes: 
- AST -> an abstract syntax tree
- root query fields
- arguments for specifying any set of fields
- Assigning variable
- Keyword: mutation, fragments, query
- Fragments: fragments are the way to group commonly used fields and reuse them.
- Query Variables: We need to write queries with the complete syntax to use query variables.
- Input types
    - Scalers such as Int, String, Float and Boolean
    - Enums
    - Arrays of the above types.
{
  arunoda: author(_id: "arunoda") {
    ...authorInfo
  },
  pahan: author(_id: "pahan") {
    ...authorInfo
  },
  indi: author(_id: "indi") {
    ...authorInfo
  }
}

fragment authorInfo on Author {
  _id,
  name,
  twitterHandle
}
