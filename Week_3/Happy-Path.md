# The Happy Path in Testing

The happy path is the path through a system where everything works, the data is correct, the system stays up, and the users are well-behaved.  We tend to test the happy path first because we understand how the system should function and want to ensure that the basic features should work.

This results in testing scenarios like this

- User selects an item and adds it to their cart
- User enters billing data
- User enters shipping data
- User clicks “Check Out”
- Transaction is processed

It doesn’t take long to test the happy path.  It takes forever to test everything off the happy path. You need to spend a lot of time wandering away from the happy path, and maybe there is a reverse rule for testing: 20% of your time on the happy path; 80% of your time off of it.