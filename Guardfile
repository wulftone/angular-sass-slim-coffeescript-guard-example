#!/usr/bin/env ruby

guard :livereload do
  watch(%r{^public/.+\.(html|js|css|png|gif|jpg)})
end

guard 'shell' do
  watch( %r{src/(.+).slim} ) { |m| `slimrb -p #{m[0]} public/#{m[1]}.html` }
end

guard 'sass', input: 'src/sass', output: 'public/css'

guard 'coffeescript', input: 'src/coffee', output: 'public/js', bare: true
