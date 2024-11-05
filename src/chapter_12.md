# Chapter 12

## Constructor & Destructor

### In C++ :

```
#include <iostream>

class human {
public:
    int height;
    int weight;
    human(int h, int w) {
        height = h;
        weight = w;
    }
    ~human(){};
    int get_height() const {
        return height;
    }
    int get_weight() const {
        return weight;
    }
};

int main() {
    human john(180, 220);
    std::cout << john.get_height() << std::endl;
    std::cout << john.get_weight() << std::endl;
    return 0;
}

```

#### Access control by Encapsulation

```

#include <iostream>

class human {
private: // abstracted from the user
    int m_h;
    int m_w;
public: 
    human(int h, int w) {
        m_h = h;
        m_w = w;
    }
    int get_h() const {
        return h;
    }
    int get_w() const {
        return w;
    }
    void set_h_w(int h, int w) {
        m_h = h;
        m_w = w;
    }

};

int main() {
    human john(180, 220);

    std::cout << john.get_h() << std::endl;
    std::cout << john.get_w() << std::endl;
    
    set_h_w(18, 22);
    
    std::cout << john.get_h() << std::endl;
    std::cout << john.get_w() << std::endl;

    return 0;
}

```