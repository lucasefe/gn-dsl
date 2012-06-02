# gn-dsl

## Description

gn-dsl is a simple dsl for (gn)[http://lucasefe.github.com/gn]

The main idea is to simplify the simplest concepts while still alowwing to do
it the original way. 

## Usage

Before

    module Plan

      class App
        
        def destination
          "app.rb"
        end

      end

    end

After

Define your plan like this:

    require 'gn/dsl'

    module Plan

      extent Gn::DSL

      template "App", "app.rb"

    end

Useful for some cases... so use as much as you want. 
