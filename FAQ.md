**Schemas**

_1.1 What is Schemas?_

Redis do not use the Schemas concept. Redis uses DB instances (0, 1, 2, 3 ... 15). So, to organize this instances and make more easy for human, we created an alias to them. These alias are Schemas.

_1.2 How many Schemas we can create?_

The DB instances, in Redis, are limited to numbers because they are just an accessory to work with a single dataset. We can create only 15 DB instances (from 0 to 14), currently. The DB15 instance is reserved to ReAdmin info\_schema.