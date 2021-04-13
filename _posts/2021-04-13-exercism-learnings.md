# What I learned from exercism

### Acronym
Everything that is not a word is regex /W/ and take out spaces in an Array

```
sentence = sentence.split(/\W/)
#To eliminate double spaces
sentence = sentence.reject { |c| c.empty? }
```

### Highscores

Max can be used in an array and attribute reader help us define a @variable

```
class HighScores
  attr_reader :scores
  
   def personal_top_three
    maxs = @scores.max(3)
    maxs.sort.reverse
   end
 end

```

### Robot

How to create random letters and how to avoid repetition of an ID

```
#Avoid id repetition
  def initialize
    loop do
      @name = generateName
      break !Robot.names_used.include?(name)
    end
    Robot.names_used << @name
  end
  
  #Generate randome letters
  (0...2).map { (65 + rand(26)).chr }.join
  
 ``` 
