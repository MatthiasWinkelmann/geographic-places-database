
require 'zlib'
require 'open-uri'
desc 'download and fix population data'
task 'cities-population.csv' do |_t|
      `wget --output-document=cities-population.csv.tar.gz 'http://data.un.org/Handlers/DownloadHandler.ashx?DataFilter=tableCode:240&DataMartId=POP&Format=csv&c=2,3,6,8,10,12,14,16,17,18&s=_countryEnglishNameOrderBy:asc,refYear:desc,areaCode:asc'`
   `tar xzf cities-population.csv.tar.gz`
   `mv UNdata* cities-population.tmp.csv`
   `rm cities-population.csv.tar.gz`
   File.open('cities-population.csv', 'w') do |out|
      IO.foreach('cities-population.tmp.csv') do |line|
         break if line.strip.empty?
         out.write line.gsub(/([^,])"([^,\n].+)/, '\\1\\2').gsub(/([^\\,])"([^,\n].+)/, '\\1\\2')
      end
   end
end
