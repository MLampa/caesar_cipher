# caesar_cipher
This is a coding challenge... to create a program that deciphers words using the Caesar cipher.

Ruby was used to complete this challenge.

```
def caesar_cipher(string, num)
  phrase = string.split("")
  shift = (num.to_i)%26
  phrase.each do |letter|
    if letter =~ (/[a-zA-Z]/)
      shift.times do
        letter.next!
      end
    end
    if letter.length > 1
      letter[0] = ""
    end
  end
  puts "'#{string}' shifted by #{num} becomes '#{phrase.join("")}'"
end

puts "Give me a word... any word."
user = gets.chomp
caesar_cipher(user, 2)
```
