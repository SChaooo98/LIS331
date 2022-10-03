# LIS331
HIVE Accelerometer code
import time
import board
import adafruit_lis331

i2c = board.I2C()  # uses board.SCL and board.SDA
lis = adafruit_lis331.LIS331HH(i2c)

while True:
    print("Acceleration : X: %.2f, Y:%.2f, Z:%.2f ms^2" % lis.acceleration)
    time.sleep(0.1)
