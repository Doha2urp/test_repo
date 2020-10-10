# A Project on GitHub and Unix bsh Programming


- The date and time of execution of make is: Sat 10 Oct 2020 01:58:03 PM +06

- The number of lines of code contained in guessinggame.sh is: 23

## Here Goes the Code

```

function guessinggame(){
fcount=$( ls | wc -l )
echo "Plese enter the file number"
while [[ $fcount -gt 0 ]]
do
	read num
	let dif=$fcount-$num
	if [[ $dif -lt -5 ]]
	then
		echo "It is too Big! Please try again"
	elif [[ $dif -gt 5 ]]
	then
		echo "It is too Low! Please try again"
	elif [[ $dif -ne 0 ]] && [[ $dif -gt -5 ]] || [[ $dif -eq -5 ]] && [[ $dif -lt 5 ]] || [[ $dif -eq 5 ]]
	then
		echo "You are very close to the answer. Please Enter it Again"
	else [[ $dif -eq 0 ]]
		echo "Congrats! its match..."
		exit	
	fi	
done
}
guessinggame

```
