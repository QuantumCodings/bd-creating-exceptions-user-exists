### Creating Exceptions

**Branch name:** creatingexceptions-prework

**RDE workflows:**
* `creatingexceptions-prework-userexistsexception`
* `creatingexceptions-prework-manageusers`
* `creatingexceptions-prework`

Expected time required: 15 min

The goal of the exercise is to create a custom `Exception` class, called `UserExistsException`,
and to utilize it in a simple service class method. A `User` POJO provided for you,
with the attributes `name`, `email` and `phoneNumber`. The service class is called `UserManager`,
which has a method `createUser(User user)` that is not complete. `createUser()`
checks to see if the user exists by calling `isEmailInUse()`. A unit test exists in `UserManagerTest`
to check the case where an email is already in use, triggering the error handling scenario you are asked
to complete using the `UserExistsException` you will create.

1) Complete the `UserExistsException` class with the 4 recommended constructors. `UserExistsException`
   should be a checked `Exception`. Set up IntellIJ to generate the `serialVersionUID` for you automatically.
   You can run the `creatingexceptions-prework-userexistsexception` workflow to test that your implementation is
   complete.

2) Update the `createUser` method provided for you in `UserManager` to throw your freshly-implemented
   `UserExistsExcpetion` if `isEmailInUse()` returns true. You can run the `creatingexceptions-prework-manageusers`
   workflow to test your change.

**You have completed this pre-work when:**
* You have implemented the `UserExistsException` class with all of its constructors.
* You have updated `createUser()` in `UserManager` to throw `UserExistsException` when a new user's email is already
  in use.
* The `creatingexceptions-prework` workflow is passing (this workflow tests both `UserExistsExcpetion` and
  `UserManager`).
* You have committed and pushed your code.
* You have answered the Canvas quiz with a link to your commit on code browser.

**HINT:**
* [How do I get IntelliJ to add the serialVersionUID?](./hints/hint-01.md)