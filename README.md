# learn_httpd_erb
This is a chef cookbook that displays html page, which describes the memory, cpu and ipaddress of the node.
For this task, Embedded Ruby is used(erb) in the template resource to display the node attributes in the index.html.erb file.

## How to run the chef cookbook
```bash
chef-client -zr "recipe[name_of_cookbook]"
```
This will run the default.rb recipe of the following cookbook and inside default.rb 'include_recipe' method is used that triggers the settings.rb file in the /learn_httpd_erb/recipe .


## How to check the syntax of recipe is correct or not
```bash
chef exec ruby -c name_of_recipe.rb

```

## Embedded Ruby
We use " <% ", if we wish to execute ruby statements.
We use " <%= " (angry squid operator), if we want ruby to print somethng.

## Passing on variable from recipe to templates
we can also pass variables from recipe to templates using 
```bash
variables(
  :x => 'any_string'
)
```

In templates we can use these variables using '@' operator.
