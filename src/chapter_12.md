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
    human obj(180, 220);
    std::cout << obj.get_height() << std::endl;
    std::cout << obj.get_weight() << std::endl;
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
        return m_h;
    }
    int get_w() const {
        return m_w;
    }
    void set_h_w(int h, int w) {
        m_h = h;
        m_w = w;
    }

};

int main() {
    human obj(180, 220);

    std::cout << obj.get_h() << std::endl;
    std::cout << obj.get_w() << std::endl;
    
    obj.set_h_w(18, 22);
    
    std::cout << obj.get_h() << std::endl;
    std::cout << obj.get_w() << std::endl;

    return 0;
}

```

#### Inheritance


```


#include <iostream>

class human {
public:
    int height;
    int weight;
public: 
    human(int h, int w) {
        height = h;
        weight = w;
    }
    int get_height() const {
        return height;
    }
    int get_weight() const {
        return weight;
    }
};

class adult : public human { // inherit from human class
public:
    std::string occupation;
public:
    adult(int h, int w) : human(h, w) {
       occupation = "doctor"; 
    } // call the base class constructor from this constructor

    std::string get_occupation() const {
        return occupation;
    }   
};

int main() {
    adult obj(180, 220);  // object of derived class
    std::cout << obj.get_occupation() << std::endl;

    obj.occupation = "lawyer";
    
    std::cout << obj.get_height() << std::endl;
    std::cout << obj.get_weight() << std::endl;
    std::cout << obj.get_occupation() << std::endl;
    
    return 0;
}

```

#### Polymorphism


```

#include <iostream>

class human {
public:
    int height;
    float weight;
    
    human(int h, int w) {
        height = h;
        weight = w;
    }
};

//print with int argument
void print(int x) {
    std::cout << x << std::endl;
}

//print with float argument
void print(float x) {
    std::cout << x  << std::endl;
}

int main() {
    human obj(180, 220);
    
    print(obj.height);
    
    print(obj.weight);
    return 0;
}

```

#### Function Polymorphism


```

#include <iostream>

class human {
public:
    int height;
    int weight;
public: 
    human(int h, int w) {
        height = h;
        weight = w;
    }
    int get_height() const {
        return height;
    }
    int get_weight() const {
        return weight;
    }
    virtual void print_all() = 0; // ()=0 creates a _pure_ virtual function that must be overridden.
    //Alternatively you can just write a default function as a virtual function with no requirement to be overwritten.
};

class adult : public human { // inherit from human class
public:
    std::string occupation;
public:
    adult(int h, int w) : human(h, w) {
       occupation = "doctor"; 
    } // call the base class constructor from this constructor

    std::string get_occupation() const {
        return occupation;
    }   

    void print_all() { // virtual function overridden in derived class
        std::cout << height << std::endl;
        std::cout << weight << std::endl;
        std::cout << occupation << std::endl;
    }
};

int main() {
    adult obj(180, 220); // object of derived class
    std::cout << obj.get_occupation() << std::endl;
    
    obj.occupation = "lawyer";
    
    obj.print_all();
    return 0;
}

```
