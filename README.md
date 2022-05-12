## For the memes
---
```cpp
auto operator ""_times(unsigned long long int x){
    return [x](int n) {
       return x*n;  
    };
}

auto operator ""_string(const char*){
    return [](int n){
      return std::to_string(n);  
    };
}

auto operator ""_you(const char*){
    return [](auto x){
      return x;  
    };
}

int main()
{
   std::cout << 4_you(5) << std::endl;
   std::cout << 2_string(42) << std::endl;
   std::cout << 5_times(42);
    return 0;
}
```
Source : https://twitter.com/vzverovich/status/1524539000656072705
