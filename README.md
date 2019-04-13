## Setting up a localhost/local server:
<pre>
1. Make directory.

2. Initiate gemfile which includes => "gem 'sinatra'" => run "bundle install".

3. Create a controller for the routing, in this example an 'app.rb'.

4. Create a 'views' directory and inside of that create an 'erb' file.

5. In your controller: 
                      - require 'sinatra/base'. 
                      - create a class which takes from takes from the Sinatra::Base.
                          (class Bob < Sinatra::Base)
                      - before the 'end' of this class ##DON'T FORGET## to add:
                          'run! if app_file == $0' 
                      - then create a 'get' method that initiates the route & calls an erb:
                          (get '/' do
                            erb :hello
                          end)
                      - this will then enable you to start the localhost, however will
                        cause error on the web page if erb is not made yet.

6. In your erb: html whatever you want.
</pre>
