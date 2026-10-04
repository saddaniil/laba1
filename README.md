#include <stdio.h>
#include <math.h>
int main() {
        for ( float x = 1.0; x <= 3.01; x += 1.3) {
                for ( float y = 2.0; y <= 4.01; y += 1.5) {
                        float z = x / (y*y);
                        float U;
                        if (z < 1.0) {
                                float a = 2.71828*(sin(x*x)) - sqrt(y);
                                float b = 1.0 / tan(cbrt(x*y*y));
                                if ( a > b) {
                                        U = a;
                                } else {
                                        U = b;
                                }
                        } else {
                                U = cos(x*y*y);
                        }
                        printf("%f %f %f\n", x, y, U);
                }
        }
        return 0;
}
