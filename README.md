```
#include <iostream>
using namespace std;

int main() {
    int n;
    double m;
    cin >> n;
    int cnt = 0;
    double a[n] = {0};

    for (int i = 0; i < n; i++) {
        cin >> m;
        a[i] = m;
    }

    for (int i = 0; i < n; i++) {
        for (int j = i; j < n; j++) {
            double sum = 0;
            for (int k = i; k <= j; k++) {
                sum += a[k];
            }
            for (int k = i; k <= j; k++) {
                if (sum / (double)(j - i+1) == a[k]) {
                    cnt++;
                    break;
                }
            }
        }
    }
    cout << cnt << endl;
    return 0;
}
```
