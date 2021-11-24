# GOAL

This is a demo to show-case how to implement a multi-step-form without any javascript and following some constraints:

* No JavaScript;
* No Gems;
* Each step must be saved in the application until the end of the form;
* Each step must validate before letting the next step to run;
* We should only save the model in the database on the last step;

This tutorial was heavily inspired on [this article](https://nicolasblanco.medium.com/developing-a-wizard-or-multi-steps-forms-in-rails-d2f3b7c692ce#.jyr0uavck) created by [Nicolas Blanco](https://github.com/nicolasblanco).

[You can also check my other demos](https://github.com/andrerferrer/dedemos/blob/master/README.md#ded%C3%A9mos).

## What needs to be done?

### 1. Create a new class to handle the validations logic

We will create a new directory: `app/models/form_models`.


we use the delegate method (from Rails ActiveSupport) to map all the attributes of the user instance inside all the view classes. By default, delegate will only delegate the reader methods. Because we also need all the setters for all attributes, we have to explicitly write it (this explains the map call you see in the Base class).



### If you want to check it locally
```sh
repo_name="multi-step-form-no-javascript-demo"
gh_repository="git@github.com:andrerferrer/$repo_name.git"
git clone $gh_repository demo
cd demo
bundle install
yarn install
rails db:create db:migrate db:seed
rails s

# now you can go to http://localhost:3000/restaurants/new and see it in action
```

And we're good to go 🤓

Good Luck and Have Fun
