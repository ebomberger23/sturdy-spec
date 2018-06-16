I/O:
```
string name = input("What is your name?");
print("Hello ", name);
```

Looping:
```
int i;
for (i=1; i<=10; i++) {
  print("Loop ", i);
}
```

Functions, if statements:
```
is_prime := function(int num) bool {
  if num < 2 {
    return false;
  }
  int i;
  for (i=2; i<num; i++) {
    if num % i == 0 {
      return false;
    }
  }
  return true;
}

int num = input("Enter a number: ").to_int();
if is_prime(num) {
  print(num, " is prime.");
}
else {
  print(num, " is not prime.");
}
```

