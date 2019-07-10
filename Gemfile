source ENV['GEM_SOURCE'] || "https://rubygems.org"

def location_for(place)
  if place =~ /^(git[:@][^#]*)#(.*)/
    [{ :git => $1, :branch => $2, :require => false }]
  elsif place =~ /^file:\/\/(.*)/
    ['>= 0', { :path => File.expand_path($1), :require => false }]
  else
    [place, { :require => false }]
  end
end

gem 'vanagon', :git => 'https://github.com/rodjek/vanagon', :branch => 'faster_rpm_dir_check'
gem 'packaging', *location_for(ENV['PACKAGING_LOCATION'] || '~> 0.99.4')
gem 'rake', '~> 12.0'

#gem 'rubocop', "~> 0.34.2"
