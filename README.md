# slot-machine

Slot Machine ~
user deposits money
user bets on 1 2 or 3 lines of slot machine
determine if they won
multiply bet by value of line
add to balance
allow to keep playing until cash out or run out of money

to-do:
collect user deposit
add deposit to balance
allow user to be on line or on multiple lines
check if user got lines correct
spin slot machine
generate diff items on slot machine/reels
add whatever won to balance
loop until user cashes out/has no more money

slice operator:
ex; current_symbols = all_symbols[:]
the ":" inside the brackets is the slice operator
this is how you copy a list
we make a copy to not make a reference and change a list/variable independently.

start by defining column list
then generate a column for every column we have
ex; for _ in range(cols):

for _ in range(rows):   <-- loop through number of values we need to generate
            value =  random.choice(current_symbols)   <-- first value is random from copied list
            current_symbols.remove(value)   <-- removes value from list so we dont pick it again
            column.append(value)   <-- add the value to our column 
columns.append(column)  <-- after for loop is finished, we should have however many rows/values so we
			add our column to our columns [list]
return columns   <--finally, return columns list


The end parameter in the print function is used to add any string.
ex; if i != len(columns) - 1:
        print(column[row], "|", end=" | ")
    else:
        print(column[row], end="")

end statement tells print statement what to end the line with
by default, end= "\n"
\n means new line character, it prints the statement to a new line.
here we add a pipe, |, at the end of our print statement.

* = splat operator/unpack operator
its going to pass every line from winning_lines list to print(f"You won on", *winning_lines) function.
ex; if we have lines 1 and 2, its going to pass both lines 1 and 2 and say "You won on 1 and 2"
