# gn-dsl

## Description

gn-dsl is a simple dsl for [gn](http://lucasefe.github.com/gn)

The main idea is to simplify the simplest concepts while still alowwing to do
it the original way. 

## Without DSL

    module Plan

      class App

        def destination
          "app.rb"
        end

      end

    end

## With DSL

Define your plan like this:

    require 'gn/dsl'

    module Plan

      extent Gn::DSL

      template "App", "app.rb"

    end

I think this is useful only on some cases. For instance, when you have many
simple templates. 

Ah, sorry, you can also do this:


    require 'gn/dsl'

    module Plan

      extent Gn::DSL

      template "App", "app.rb" do
        def name
          "My App Name"
        end
      end

    end
