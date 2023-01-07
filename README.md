# code-test-2020-v6

code-test-2020-v6

My Review;

The structure used in the code is a repository pattern, in which we create repositories for each entity like we create models and write all the logic inside repositories. From the controller we just pass data to repository methods, do CRUD on it and get the return.

I can say this structure will be good for large-scale applications on which so many hands will be working and so many automated tests will be required. Because it helps too much in defining rules for code to follow SOLID principles and support unit tests.
It is good to use when we want to make our application easily testable using unit tests.
This pattern is more friendly while implementing SOLID principles like the single responsibility principle and dependency inversion principle.
We can make much reusable code if there are so many CRUD operations by making a generic interface for all CRUD entities.
Using this developer can keep the same approach or a rule-based code to be followed by all the developers by making interfaces, about interfaces we can sets of rules which can be implemented in repositories.

But

We have to do some more effort for the same job which can easily be done using the Active record pattern.
It creates an extra Abstraction layer over the code.
In repositories, we can only implement CRUD confidently not too much logic, and if have implemented any interface in a repository then we are bounded to follow the rules.
For example, if have passed some params to a repository method that is using an interface, and we get some changes in params and return for a specific function then we have to change the interface rule for the method and then the repository too, and if that interface is implemented by some other entities repositories then we have to change all that too. In this way, the repository pattern becomes very difficult to maintain.
In Short Active record pattern is fast, easy, and simple, but models and controllers become FAT if we will use them for large-scale projects.
