# Rovixcloud
api for rovixcloud.com fre temp email site
# main
```cpp
#include "Rovixcloud.h"
#include <iostream>

int main() {
   Rovixcloud api;
    auto email = api.generate_email().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    email.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
