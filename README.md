
##Сборка
1. cargo build --release
2. cargo objcopy --bin stm32f103c8t6 --target thumbv7m-none-eabi --release -- -O binary stm32f1.bin
##Прошивка
1. Проверка подключения st-info --descr. Должно быть "F1 Medium-density device"
2. Очищаем flash память st-flash erase
3. Загружаем прошивку st-flash write stm32f1.bin 0x8000000