# Получение сведений о системе
Смирнов Михаил

# Системы аутентификации и защиты от несанкционированного доступа

## Лабораторная работа №1

## Цель работы

Получить сведения об используемой системе

## Исходные данные

1.  ОС Windows 10
2.  WSL2
3.  Ноутбук ASUS

## План

1.  Выполнить команду uname -r
2.  Выполнить команду cat /proc/cpuinfo | grep “model name”
3.  Выполнить команду journalctl -q -b | tail -n 30

## Ход работы

1\. Первым шагом выполним команду uname -r для вывода информации о
системе.

``` bash
uname -r
```

    5.15.90.1-microsoft-standard-WSL2

2\. Далее выполним команду cat /proc/cpuinfo | grep “model name” для
вывода информации о процессоре, строки которой содержат “model name”.

``` bash
cat /proc/cpuinfo | grep "model name"
```

    model name  : AMD Ryzen 5 4500U with Radeon Graphics
    model name  : AMD Ryzen 5 4500U with Radeon Graphics
    model name  : AMD Ryzen 5 4500U with Radeon Graphics
    model name  : AMD Ryzen 5 4500U with Radeon Graphics
    model name  : AMD Ryzen 5 4500U with Radeon Graphics
    model name  : AMD Ryzen 5 4500U with Radeon Graphics

3\. Позже выполним команду dmesg | tail -n 30 для вывода последних 30
строк логов.

``` bash
dmesg | tail -n 30
```

    [    3.487442] EXT4-fs (sdc): mounted filesystem with ordered data mode. Opts: discard,errors=remount-ro,data=ordered. Quota mode: none.
    [    4.371070] hv_pci 3f01c7d9-220a-4acf-9c25-8f4522f89d82: PCI VMBus probing: Using version 0x10003
    [    4.373663] hv_pci 3f01c7d9-220a-4acf-9c25-8f4522f89d82: PCI host bridge to bus 220a:00
    [    4.374434] pci_bus 220a:00: root bus resource [mem 0x9ffe08000-0x9ffe0afff window]
    [    4.376389] pci_bus 220a:00: No busn resource found for root bus, will use [bus 00-ff]
    [    4.378887] pci 220a:00:00.0: [1af4:1049] type 00 class 0x010000
    [    4.381139] pci 220a:00:00.0: reg 0x10: [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.382793] pci 220a:00:00.0: reg 0x18: [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.384415] pci 220a:00:00.0: reg 0x20: [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    4.392055] pci_bus 220a:00: busn_res: [bus 00-ff] end is updated to 00
    [    4.392676] pci 220a:00:00.0: BAR 0: assigned [mem 0x9ffe08000-0x9ffe08fff 64bit]
    [    4.394088] pci 220a:00:00.0: BAR 2: assigned [mem 0x9ffe09000-0x9ffe09fff 64bit]
    [    4.395512] pci 220a:00:00.0: BAR 4: assigned [mem 0x9ffe0a000-0x9ffe0afff 64bit]
    [    4.612945] hv_pci ce110406-dfa4-439a-9346-7b36f942ee1a: PCI VMBus probing: Using version 0x10003
    [    4.615575] hv_pci ce110406-dfa4-439a-9346-7b36f942ee1a: PCI host bridge to bus dfa4:00
    [    4.616379] pci_bus dfa4:00: root bus resource [mem 0x9ffe0c000-0x9ffe0efff window]
    [    4.617137] pci_bus dfa4:00: No busn resource found for root bus, will use [bus 00-ff]
    [    4.619840] pci dfa4:00:00.0: [1af4:1049] type 00 class 0x010000
    [    4.622286] pci dfa4:00:00.0: reg 0x10: [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    4.624316] pci dfa4:00:00.0: reg 0x18: [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    4.626231] pci dfa4:00:00.0: reg 0x20: [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    4.638517] pci_bus dfa4:00: busn_res: [bus 00-ff] end is updated to 00
    [    4.639255] pci dfa4:00:00.0: BAR 0: assigned [mem 0x9ffe0c000-0x9ffe0cfff 64bit]
    [    4.640920] pci dfa4:00:00.0: BAR 2: assigned [mem 0x9ffe0d000-0x9ffe0dfff 64bit]
    [    4.643182] pci dfa4:00:00.0: BAR 4: assigned [mem 0x9ffe0e000-0x9ffe0efff 64bit]
    [    5.018580] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    5.037356] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    5.040734] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    5.044196] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -22
    [    5.068864] misc dxg: dxgk: dxgkio_query_adapter_info: Ioctl failed: -2

## Оценка результата

В результате лабораторной работы №1 мы получили основную информацию об
ОС и процессоре и логи системы.

## Вывод

Таким образом, мы научились работать с базовыми командами Linux и
получать информацию об операционной системе.
