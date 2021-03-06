## 一个简单的矩阵模板类实现
#### 成员函数
```cpp
 //Constructors
Matrix();
Matrix(int row, int column);
Matrix(int row, int column, T val);
Matrix(Matrix const& secondMatrix);
virtual ~Matrix();   //Destructor shoule be declared as virtual unless it won't be inheritanced

//Basic operation
int getRow() const;
int getColumn() const;
T getValue(int x, int y) const;
void setValue(int x, int y,T val);
void show();

//Math operation
Matrix add(Matrix const& secondMatrix) const;
Matrix subtract(Matrix const& secondMatrix) const;
Matrix multiply(Matrix const& secondMatrix) const;

//Operator overloading
Matrix& operator=(Matrix const& secondMatrix);
Matrix operator+(Matrix const& secondMatrix) const;
Matrix operator-(Matrix const& secondMatrix) const;
Matrix operator*(Matrix const& secondMatrix) const;
Matrix operator+=(Matrix const& secondMatrix);
Matrix operator-=(Matrix const& secondMatrix);
Matrix operator*=(Matrix const& secondMatrix);
T* operator[](int x) const;
 ```
  
  #### 数据成员
  ```cpp
  
  int row;
  int column;
  T **value;

  void initialize();     //Initialize Matrix & allocate memory
  ```
