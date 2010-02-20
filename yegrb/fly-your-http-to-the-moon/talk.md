!SLIDE

# Fly your HTTP to the moon

Sinatra in 10 minutes

!SLIDE

# Daniel Huckstep

Software engineer (EIT)

[http://blog.darkhax.com/](http://blog.darkhax.com/)

[@darkhelmetlive](http://twitter.com/darkhelmetlive)

!SLIDE

# Sinatra
...it's awesome

!SLIDE center

![sinatra](sinatra.jpg)

!SLIDE center

![sinatra-web](sinatra-web.png)

!SLIDE

## Fast &rarr; Simple &rarr; Easy

!SLIDE

# Obligatory 'Hello, World!'

!SLIDE

@@@ ruby
    require 'rubygems'
    require 'sinatra'

    get '/' do
      'Hello, World!'
    end
@@@

!SLIDE

## > HTTP Methods
## Static Files and Views
## Routing and Parameters
## Helpers and Filters
## Configuration and Error Handling
## Middleware and Testing
## Gang Vocals (All together now!)

!SLIDE

@@@ ruby
    get '/' do
      # Also creates a HEAD handler
      "Gettin' somethin'..."
    end

    post '/' do
      "Creatin' somethin'..."
    end
@@@

!SLIDE

@@@ ruby
    put '/' do
      "Updatin' somethin'..."
    end

    delete '/' do
      "Deletin' somethin'..."
    end
@@@

!SLIDE

## HTTP Methods
## > Static Files and Views
## Routing and Parameters
## Helpers and Filters
## Configuration and Error Handling
## Middleware and Testing
## Gang Vocals (All together now!)

!SLIDE

@@@ ruby
    require 'haml'

    get '/' do
      haml(:index)
    end
@@@

!SLIDE

@@@ ruby
    require 'erb'

    get '/' do
      erb(:index)
    end
@@@

!SLIDE

@@@ ruby
    require 'erubis'

    get '/' do
      erubis(:index)
    end
@@@

!SLIDE

@@@ ruby
    require 'builder'

    get '/' do
      builder(:index)
    end
@@@

!SLIDE

@@@ ruby
    require 'haml'

    get '/style.css' do
      sass(:style)
    end
@@@

!SLIDE

## HTTP Methods
## Static Files and Views
## > Routing and Parameters
## Helpers and Filters
## Configuration and Error Handling
## Middleware and Testing
## Gang Vocals (All together now!)

!SLIDE

@@@ ruby
    get '/archive/:year/:month/:day/:title' do |year, month, day, title|
       @post = Post.find(...)
       haml(:post, :locals => { :post => @post })
    end
@@@

!SLIDE

# Questions?
# Comments?

!SLIDE

# ...Cookies?