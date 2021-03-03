2-5. '*'문자로 정사각형, 직사각형, 삼각형의 형태를 출력해보세요
```c++
// 정사각형
void Square()
{
    int side;
    
    cout << "정사각형 출력하기" << endl;
    cout << "Please enter side : ";
    cin >> side;

    for (int i = 0; i < side;++i) {
        for (int j = 0; j < side; ++j) {
            cout << "*";
        }
        cout << endl;
    }
    

}
```
```c++
// 직사각형
void Rectangle()
{
    int base, height;

    cout << "직사각형 출력하기" << endl;
    cout << "Please enter base : ";
    cin >> base;
    cout << "Please enter height : ";
    cin >> height;

    for (int i = 0; i < height; ++i) {
        for (int j = 0; j < base; ++j) {
            cout << "*";
        }
        cout << endl;
    }

}
```
```c++
// 삼각형
void Triangle()
{
    int side;

    cout << "삼각형 출력하기" << endl;
    cout << "Please enter side : ";
    cin >> side;

    int j, k;
    for (int i = 0; i < side; i++) {
        for (j=0 ; j < side-i-1; j++) {
            cout << " ";
        }
        for (k = 0; k < side-j; k++) {
            cout << "*";
        }
        for (k = 0; k < side - j-1; k++) {
            cout << "*";
        }
        cout << endl;
    }

}
```
