<p align="center">
  <img width="100" height="100" src="https://github.com/g00dvin/continent-faq/blob/master/res/logo.jpg">
</p>
# АПКШ Континент
> Так или иначе, но тебе повезло и ты нашел этот документ. Тут мы постараемся рассказать тебе о том, что поможет тебе в дальнейшем не страдать, а получать удовольствие при использовании АПКШ Континент.

---

## Версии программного обеспечения
На текущий момент актуальной является версия АПКШ Континент 3.7.7.

|Версия|Статус|Последний сертифицированный билд|
| --- | --- | --- |
| 3.5 | EOL | 3.5.74.0 |
| 3.6 | EOL | 3.6.90.4 |
| **3.7** | **Текущая** | **3.7.7.671** |
| 3.9 | Сертификация | 3.9.2880 |
| 4 | В разработке | Не зафиксировано |

## Аппаратные платформы
| Модель | Шасси | Поддерживаемые версии ПО |
|--- | --- | --- |
| IPC10 | S088| 3.7, 3.9 |
| IPC10 | LN010A | 3.7, 3.9, 4 |
| IPC10 | S185 | 3.9, 4 |
| IPC25 | GA630 | 3.5, 3.6 |
| IPC25 | 9830 | 3.5, 3.6 |
| IPC25 | 92D9 | 3.6, 3.7, 3.9 |
| IPC25 | S115 | 3.7, 3.9, 4* |
| IPC50 | LN010C | 3.9, 4 |
| IPC100 | G560 | 3.5, 3.6 |
| IPC100 | 92E3 | 3.6, 3.7, 3.9 |
| IPC100 | S102 | 3.6, 3.7, 3.9, 4* |
| IPC400 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC400 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC500 | LN015B | 3.7, 3.9, 4 |
| IPC500F | LN015C | 3.9, 4 |
| IPC600 | DV030A | 3.9, 4 |
| IPC800F | DV030B | 3.9, 4 |
| IPC1000 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000F | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000F2 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1010 | IBM9297 | 3.6, 3.7, 3.9 |
| IPC1000 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000F2 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC1000 | DV031A | 3.9, 4 |
| IPC1000F | DV031B | 3.9, 4 |
| IPC1000F2 | DV031C | 3.9, 4 |
| IPC3000F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3034 | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3034F | S021 | 3.6, 3.7, 3.9, 4* |
| IPC3000F | LN021 | 3.9, 4 |
| IPC3000FC | LN021A | 3.9, 4 |
| IPC3000NF2 | LN021E | 3.9, 4 |
| IPC3034F | LN021C | 3.9, 4 |
| IPC3000 | LN021D | 3.9, 4 |
| IPC5000FC | S145 | 3.9, 4 |

*\* требуется приобретение комплекта модернизации RAM и HDD, подробности уточнять у вендора.*

## Инсталляция ПО
АПКШ Континент, в случае его приобретения, поставляется с предустановленной, на производстве Кода Безопасности, текущей тиражируемой версией ПО. В некоторых случая может потребоваться переустановка ПО (понижение или повышение версии, восстановление работоспособности, установка отладочной версии по и т.д.).

### Инсталляция на аппаратную платформу
При инсталляции ПО на аппаратную платформу используются два источника инсталляции:
* CD-диск (входит в комплекте поставки оборудования)
* USB Flash drive (так же входит в состав поставки)

Самый распространенный способ - это установка через USB Flash drive. В этом случае на носитель необходимо записать образ USB Flash drive из комплекта поставки, образы находятся на CD-диске в директории Setup\Continent\FLASH\IMAGES, имеют расширение .flash и записываются на USB Flash drive при помощи таких утилит как dd (Linux), [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/), [Rufus](https://rufus.ie/ru_RU.html) (Windows). По факту каждый образ это raw image жесткого диска с двумя разделами, первый раздел FAT размером 8 МБ предназначен для сохранения ключей администратора ЦУС или же конфигурации и ключей КШ, второй раздел UFS (FreeBSD) содержит необходимые для установки ПО файлы. Созданный таким образом USB Flash drive будет являться загрузочным устройством и позволит произвести установку ПО на аппаратную платформу АПКШ.

Каждый образ установочного ПО содержит требуемый функционал для конкретной реализации ПО:

* arm_release.flash - АРМ ГК (Генерации Ключей)
* cgw.aserv_release.flash - КШ-СД
* cgw_release.flash - КШ
* csw_release.flash - КК
* ids_release.flash - ДА
* ncc.aserv_release.flash - ЦУС-СД
* ncc_release.flash - ЦУС

