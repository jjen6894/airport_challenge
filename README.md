__Incomplete__
With the users stories, I am looking to set up three classes; Airport, Plane and Weather_report. Having each class with their required methods. Start off small showing the first test to check each class exist and each has their first method; (initialize, for Plane and Airport). The first user story wants to instruct a plane to land in an airport and then confirm its landed. To do this I would create a land method within the plane class and a planes_in_airport array to contain those landed, this will allow to confirm by print the lastest value enter into the array aka the plane that had just landed confirming it has. 

The second user story ask me to make planes take off from airports then confirm it is no longer in the airport, this will mean that similarily to the landing method, this will also be created in the plane class, this is due to my belief that it is a attribute of a plane class rather than airport. To confirm we would then either print the value of flying or show the new list of planes_in_airport with the one less or even empty.

Third user story asks us to ensure safety to not allow planes to take off when weathr is stormy. This needs a few implementions of code, one would be the creation of the stormy method where weather produces a random number 1..6 and if the number is 6 then stormy is true. This will give stormy a 1 in 6 chance of happening as it is rare. Along with this creation using this method to check first before activating the take off method from running if stormy is true and therefore raise and error upon this happening.

The next is very similar using the same technique to check before landing if weather is stormy this will be a one line boolean check where if stormy is true there method won't execute else carry on as normally all implicity implied with the one line.

another safety test these will all be under the sub heading context safety for the tests, this will allow me to read what is passing and failing a lot easier, this safety test is referring back to the planes_in_airport array this will now need a dafeault capacity in order to know if its empty, full and hold values of recently landed planes and deleting those that take off. This will be very similar to the stormy code as it will be however within the airport class in a private methods, both are never going to be called on planes or weather therefore its could practice to keep them within and only used by airport. 


Airport Challenge
=================

```
        ______
        _\____\___
=  = ==(____MA____)
          \_____\___________________,-~~~~~~~`-.._
          /     o o o o o o o o o o o o o o o o  |\_
          `~-.__       __..----..__                  )
                `---~~\___________/------------`````
                =  ===(_________)

```

Instructions
---------

* Challenge time: rest of the day and weekend, until Monday 9am
* Feel free to use google, your notes, books, etc. but work on your own
* If you refer to the solution of another coach or student, please put a link to that in your README
* If you have a partial solution, **still check in a partial solution**
* You must submit a pull request to this repo with your code by 9am Monday morning

Steps
-------

1. Fork this repo, and clone to your local machine
2. Run the command `gem install bundle` (if you don't have bundle already)
3. When the installation completes, run `bundle`
4. Complete the following task:

Task
-----

We have a request from a client to write the software to control the flow of planes at an airport. The planes can land and take off provided that the weather is sunny. Occasionally it may be stormy, in which case no planes can land or take off.  Here are the user stories that we worked out in collaboration with the client:

```
As an air traffic controller 
So I can get passengers to a destination 
I want to instruct a plane to land at an airport and confirm that it has landed 

As an air traffic controller 
So I can get passengers on the way to their destination 
I want to instruct a plane to take off from an airport and confirm that it is no longer in the airport

As an air traffic controller 
To ensure safety 
I want to prevent takeoff when weather is stormy 

As an air traffic controller 
To ensure safety 
I want to prevent landing when weather is stormy 

As an air traffic controller 
To ensure safety 
I want to prevent landing when the airport is full 

As the system designer
So that the software can be used for many different airports
I would like a default airport capacity that can be overridden as appropriate
```

Your task is to test drive the creation of a set of classes/modules to satisfy all the above user stories. You will need to use a random number generator to set the weather (it is normally sunny but on rare occasions it may be stormy). In your tests, you'll need to use a stub to override random weather to ensure consistent test behaviour.

Your code should defend against [edge cases](http://programmers.stackexchange.com/questions/125587/what-are-the-difference-between-an-edge-case-a-corner-case-a-base-case-and-a-b) such as inconsistent states of the system ensuring that planes can only take off from airports they are in; planes that are already flying cannot takes off and/or be in an airport; planes that are landed cannot land again and must be in an airport, etc.

For overriding random weather behaviour, please read the documentation to learn how to use test doubles: https://www.relishapp.com/rspec/rspec-mocks/docs . There’s an example of using a test double to test a die that’s relevant to testing random weather in the test.

Please create separate files for every class, module and test suite.

In code review we'll be hoping to see:

* All tests passing
* High [Test coverage](https://github.com/makersacademy/course/blob/master/pills/test_coverage.md) (>95% is good)
* The code is elegant: every class has a clear responsibility, methods are short etc. 

Reviewers will potentially be using this [code review rubric](docs/review.md).  Referring to this rubric in advance will make the challenge somewhat easier.  You should be the judge of how much challenge you want this weekend.

**BONUS**

* Write an RSpec **feature** test that lands and takes off a number of planes

Note that is a practice 'tech test' of the kinds that employers use to screen developer applicants.  More detailed submission requirements/guidelines are in [CONTRIBUTING.md](CONTRIBUTING.md)

Finally, don’t overcomplicate things. This task isn’t as hard as it may seem at first.

* **Submit a pull request early.**  There are various checks that happen automatically when you send a pull request.  **Fix these issues if you can**.  Green is good.

* Finally, please submit a pull request before Monday at 9am with your solution or partial solution.  However much or little amount of code you wrote please please please submit a pull request before Monday at 9am.
