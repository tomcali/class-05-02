* **Instructions:**

* Spend the next few minutes with your partner answering the following questions. You should be using the Sequelize Documentation (and whatever other references you find online).

  ```
  	- Answer: What is Sequelize?  object-relational mapper that works with mysql, mariadb, sqlite, postgres, and sqlserver

  	- Answer: What advantages does it offer?  easier syntax, works across various database systems

  	easy to test 
  	gives you support for syncing databases
  	validation  restricts to specific form of data
  	complex sql queries in simple syntax

  	- Answer: How do I install it? How do I incorporate it into my app?  npm install --save sequelize

  	- Answer: What the heck is a Sequelize model? What role will it play?  general relational database specs, with types for columns that work across databases such as string and text integer 

  	- Answer: Let's say I have the below table in MySQL. 

  		| Country     | PhoneCode | Capital   | IndependenceYear |
  		|-------------|-----------|-----------|------------------|
  		| Afghanistan | 93        | Kabul     | 1919             |
  		| Belarus     | 375       | Misk      | 1991             |
  		| Netherlands | 31        | Amsterdam | 1648             |
  		| Oman        | 968       | Muscat    | 1970             |
  		| Zambia      | 260       | Lusaka    | 1964             |

  		- How would I model it in Sequelize?  string integer column data types

  		- How would I query for all the records where the Independence Year was less than 50 years ago?  find by id or findAll

  		var tablename - sequelize.define('tablename', {
  		country: {
  		type: Sequelize: STRING
  		},
  		PHONECODE: {
  		type: Sequelize: STRING
  		},
  		Capital: {
  		type: Sequelize: STRING
  		}
  		IndependenceYear: {
  		type: Sequelize: INTEGER
  		},
  		}
  		{
  		freezeTableName: true //  
  		}

  		- How would I query the table, order it by descending Independence Years, and limit the results to just show 2 of the records. Skipping the first two? (i.e. Results: Zambia, Afghanistan)   findAll *   order: 'CountryIndependenceYear DESC'

  		tableName.findAll
  		where independenceYear: {$gt: now Date().getFullYear() - 50)
  		}
  		});
  		
  		

  	- Bonus: How do I use Sequelize to make changes to an existing table with data in it? 
After createTable... try updating with statements like this:
addColumn
changeColumn
removeColumn
addIndex
removeIndex
addConstraint
removeConstraint
  ```
