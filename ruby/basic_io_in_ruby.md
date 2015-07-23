### 1. Inside File.open

```ruby
class File
	def File.open(*args)
		result = f = File.new(*args)
		if block_given?
			begin
				result = yield f
			ensure
				f.close
			end
		end
		result
	end
end
```

### 2. Retrieve an entire file into a string or into an array of lines

```ruby
# read into string
str = IO.read("testfile")
str.length # => 66
str[0, 30] # => "This is line one\nThis is line "

# read into an array
arr = IO.readlines("testfile")
arr.length # => 4
arr[0]
# => "This is line one\n"
```