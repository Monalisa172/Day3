# Day3

Qs:1
fun main() {
    val n = 5 
    for (i in 1..n) {
        for (j in 1..n - i) {
            print(" ") 
        }
        for (k in 1..(2 * i - 1)) {
            print("*") 
        }
        println()
    }
    for (i in n downTo 1) {
        for (j in 1..n - i) {
            print(" ")
        }
        for (k in 1..(2 * i - 1)) {
            print("*") 
        }
        println()
    }

}

Qs:2 
fun main(args: Array<String>) {
    val num = 125
    var originalNum: Int
    var rem: Int
    var result = 0
    originalNum = num
    while (originalNum!= 0) {
        rem = originalNum % 10
        result += Math.pow(rem.toDouble(), 3.0).toInt()
        originalNum/= 10
    }
    if (result == num)
        println("$num is an Armstrong number.")
    else
        println("$num is not an Armstrong number.")
}


Qs:3
fun main() {
   var num1=50;
   var num2=50;
   var gcd = 1;
   println("enter the value of a is $num1");
   println("enter the value of b is $num2");
   var i = 1
   while (i <= num1 && i <= num2) {
      if (num1 % i == 0 && num2 % i == 0)
         gcd = i
      i++
   }
println("The result is $gcd")
}


Qs:4
fun main() {
    val input = "Kotlin is Amazing!"
    val frequencyMap = mutableMapOf<Char, Int>()
    for (char in input) {
        if (char.isLetter()) {
            val lowercaseChar = char.lowercaseChar() 
            frequencyMap[lowercaseChar] = frequencyMap.getOrDefault(lowercaseChar, 0) + 1
        }
    }
    println("Frequency of letters in '$input':")
    for ((char, count) in frequencyMap) {
        println("$char: $count")
    }
}


Qs:5
fun DuckNumber(number: String): Boolean {
    if (number.startsWith('0')){
    return false   
    }
    return number.substring(1).contains('0')
}
fun main() {
    val testNumbers = listOf("088", "3000", "5")
    for(num in testNumbers) {
        if (DuckNumber(num)) {
            println("$num is a duck number.")
        } else {
            println("$num is not a duck number.")
        }
    }
}
