# Neo4j Basics

Neo4j is a graph database, which means that all the entities are modeled with Nodes and relationships. To better illustrate this, let's look at an example and see how we can model the entities with nodes and relationships. Let's say that you are making an app that allows users to post food recipes. From that very sentence you can easily see that you are going to have a lot of users and recipes in your app. And there you have it, you will need a lot of `User` and `Recipe` nodes. Furthermore, each user will own a recipe, so you are going to have a `OWNS_RECIPE` relationship between users and recipes. In addition to ownerships, a user might favorite a recipe as well which results in another relationship between users and recipes. As you can see, thinking about nodes and relationships are very natural, and Neo4j provides a custom query language that makes working with Neo4j very straightforward. Neo4j's custom query language is called Cypher which can be used to create nodes, relationships, investigate relationships and so on. In the next sections we will learn how to user Cypher.

## Creating a Node

To create a node, we can use the `CREATE` query. Let's create a user whose name is Tom:

```
CREATE(u: User {name: 'Tom'});
```

Let's break down this query:

- `CREATE()` is the main query for creating nodes.
- `u: User`: means that `u` is like a variable that references the new node that is going to be created. What follows the references is the label. You can think of a label as a type.
- `{name: 'Tom'}`: Using this syntax we are defining the properties of the user node. We are creating a name property whose value is the string `Tom`

You can try this query and run it in the Neo4j browser interface and you should be able to see a new node created in the database.

