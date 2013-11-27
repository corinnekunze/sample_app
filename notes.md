.inspect returns the LITERAL notation of the object.

puts :name, :name.inspect
	name
	:name

	p :name   # Same as 'puts :name.inspect'

>> s = "foobar"       # A literal constructor for strings using double quotes
=> "foobar"
>> s.class
=> String

These are identical

>> s = String.new("foobar")   # A named constructor for a string
=> "foobar"
>> s.class
=> String
>> s == "foobar"
=> true

===============

>> class Word < String             # Word inherits from String.
>>   # Returns true if the string is its own reverse.
>>   def palindrome?
>>     self == self.reverse        # self is the string itself.
>>   end
>> end

makes sure that Word has all the methods that String does.

=================
bundle exec rake test:prepare

This just ensures that the data model from the development database, db/development.sqlite3, is reflected in the test database, db/test.sqlite3.9 (Failure to run this Rake task after a migration is a common source of confusion. In addition, sometimes the test database gets corrupted and needs to be reset. If your test suite is mysteriously breaking, be sure to try running rake test:prepare to see if that fixes the problem.)