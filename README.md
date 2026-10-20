# device_xiaomi_sm8750_common

Xiaomi SM8750 (Snapdragon 8 Elite) platformunun **ortak** katmanı — cihazdan
bağımsız, cihazlar arası paylaşılan ayarlar.

## İçerik

```
common.mk                              ortak ürün tanımları
configs/audio/
  audio_policy_configuration.xml       ses policy'si
  bluetooth_audio_policy_configuration.xml
```

## Kullanım

```make
$(call inherit-product, device/xiaomi/sm8750-common/common.mk)
```

`device/xiaomi/xuanyuan/device.mk` bu dosyayı inherit eder.

## Neden ayrı repo?

Aynı SoC üzerindeki diğer Xiaomi cihazları (kodename farklı olsa da) ses
policy'si ve Bluetooth yapılandırması açısından ortak noktalar taşır.
Ortak katmanı ayırmak, cihaz özel değişikliklerin cihaz ağacında kalmasını
ve platform değişikliklerinin tek yerde toplanmasını sağlar.

## Lisans

Apache-2.0.
