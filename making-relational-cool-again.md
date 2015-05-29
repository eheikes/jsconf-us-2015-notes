# "Making Relational Cool Again" by [Tim Griesser](https://twitter.com/tgriesser)

This talk was about using relational DBs in NodeJS, specifically the speaker's 2 libraries.

* There are similarities between SQL and JS.
  * Both are languages that will never die.
* Rise of NoSQL & the hate against relational DBs
* Existing SQL module ecosystem
  * Usually DB-specific
  * Mixes ORM and query layers
  * No transaction API
* [Knex.js](http://knexjs.org/) SQL query builder
  * Unified SQL language
  * Transactions are part of the promise chain
  * Nested transactions
* [Bookshelf.js](http://bookshelfjs.org/) ORM
  * Supports relationships
* Knex + Bookshelf integration
  * Can drop into Knex from Bookshelf
  * Bookshelf has some transaction support
* Shared models (isomorphic JS): not as great in practice
* Alternatives: OpenRecord, Sequelize, azul.js, SQL Bricks, etc.
* Summary
  * Reinvent the wheel. (Don't be afraid to try and make a better wheel.)
  * Get ideas from other languages.
  * Use Node for more CRUD apps.
