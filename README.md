# Libft - 42 School C Library

> 42 School müfredatının ilk projesi: C dilinde standart kütüphane fonksiyonlarının yeniden yazılması.

## 📋 İçindekiler

- [Proje Hakkında](#-proje-hakkında)
- [Fonksiyonlar](#-fonksiyonlar)
- [Kurulum](#-kurulum)
- [Kullanım](#-kullanım)
- [Test](#-test)
- [Kaynaklar](#-kaynaklar)

---

## 🎯 Proje Hakkında

**Libft**, 42 School'un temel C programlama projesidir. Bu projede, standart C kütüphanesinde (`libc`) bulunan fonksiyonların yanı sıra gelecek projelerde kullanılacak yardımcı fonksiyonlar sıfırdan yazılmaktadır.

### Öğrenilen Kavramlar

- Bellek yönetimi (`malloc`, `free`)
- İşaretçi (pointer) manipülasyonu
- Statik kütüphane oluşturma (`.a` dosyası)
- Makefile yazımı
- Linked list veri yapısı

---

## 📚 Fonksiyonlar

### Libc Fonksiyonları

| Fonksiyon | Açıklama |
|-----------|----------|
| `ft_isalpha` | Karakterin alfabetik olup olmadığını kontrol eder |
| `ft_isdigit` | Karakterin rakam olup olmadığını kontrol eder |
| `ft_isalnum` | Karakterin alfanümerik olup olmadığını kontrol eder |
| `ft_isascii` | Karakterin ASCII tablosunda olup olmadığını kontrol eder |
| `ft_isprint` | Karakterin yazdırılabilir olup olmadığını kontrol eder |
| `ft_strlen` | String uzunluğunu hesaplar |
| `ft_memset` | Bellek bloğunu belirli bir değerle doldurur |
| `ft_bzero` | Bellek bloğunu sıfırlar |
| `ft_memcpy` | Bellek bloğunu kopyalar |
| `ft_memmove` | Bellek bloğunu güvenli şekilde taşır |
| `ft_strlcpy` | String'i güvenli şekilde kopyalar |
| `ft_strlcat` | String'i güvenli şekilde birleştirir |
| `ft_toupper` | Küçük harfi büyük harfe çevirir |
| `ft_tolower` | Büyük harfi küçük harfe çevirir |
| `ft_strchr` | String içinde karakter arar (baştan) |
| `ft_strrchr` | String içinde karakter arar (sondan) |
| `ft_strncmp` | İki string'i karşılaştırır |
| `ft_memchr` | Bellek bloğunda karakter arar |
| `ft_memcmp` | İki bellek bloğunu karşılaştırır |
| `ft_strnstr` | String içinde alt string arar |
| `ft_atoi` | String'i integer'a çevirir |
| `ft_calloc` | Bellek tahsis eder ve sıfırlar |
| `ft_strdup` | String'i kopyalar (yeni bellek tahsisi ile) |

### Ek Fonksiyonlar

| Fonksiyon | Açıklama |
|-----------|----------|
| `ft_substr` | Alt string oluşturur |
| `ft_strjoin` | İki string'i birleştirir |
| `ft_strtrim` | String'in başından ve sonundan karakterleri kırpar |
| `ft_split` | String'i ayırıcıya göre böler |
| `ft_itoa` | Integer'ı string'e çevirir |
| `ft_strmapi` | String'e fonksiyon uygular (yeni string döner) |
| `ft_striteri` | String'e fonksiyon uygular (yerinde değiştirir) |
| `ft_putchar_fd` | Karakteri file descriptor'a yazar |
| `ft_putstr_fd` | String'i file descriptor'a yazar |
| `ft_putendl_fd` | String'i newline ile file descriptor'a yazar |
| `ft_putnbr_fd` | Sayıyı file descriptor'a yazar |

### Bonus: Linked List Fonksiyonları

| Fonksiyon | Açıklama |
|-----------|----------|
| `ft_lstnew` | Yeni liste elemanı oluşturur |
| `ft_lstadd_front` | Listenin başına eleman ekler |
| `ft_lstsize` | Liste boyutunu döner |
| `ft_lstlast` | Listenin son elemanını döner |
| `ft_lstadd_back` | Listenin sonuna eleman ekler |
| `ft_lstdelone` | Tek bir liste elemanını siler |
| `ft_lstclear` | Tüm listeyi temizler |
| `ft_lstiter` | Listeye fonksiyon uygular |
| `ft_lstmap` | Listeye fonksiyon uygular (yeni liste döner) |

---

## ⚙️ Kurulum

### Gereksinimler

- GCC derleyici
- Make
- Unix tabanlı işletim sistemi (Linux/macOS)

### Derleme

```bash
# Repository'yi klonla
git clone https://github.com/KULLANICI_ADI/libft.git

# Dizine gir
cd libft

# Kütüphaneyi derle
make

# Bonus fonksiyonları dahil et
make bonus

# Temizlik
make clean    # .o dosyalarını sil
make fclean   # .o ve .a dosyalarını sil
make re       # Yeniden derle
```

---

## 🚀 Kullanım

### Projenize Dahil Etme

```c
// Header dosyasını include edin
#include "libft.h"

int main(void)
{
    char *str;
    
    // ft_strdup kullanımı
    str = ft_strdup("Merhaba, 42!");
    ft_putendl_fd(str, 1);
    
    // ft_strlen kullanımı
    ft_putnbr_fd(ft_strlen(str), 1);
    
    free(str);
    return (0);
}
```

### Derleme

```bash
gcc -Wall -Wextra -Werror main.c -L. -lft -o program
```

---

## 🧪 Test

### Popüler Test Araçları

| Test | Link |
|------|------|
| libft-unit-test | [github.com/alelievr/libft-unit-test](https://github.com/alelievr/libft-unit-test) |
| libftTester | [github.com/Tripouille/libftTester](https://github.com/Tripouille/libftTester) |
| libft-war-machine | [github.com/0x050f/libft-war-machine](https://github.com/0x050f/libft-war-machine) |

### Test Çalıştırma

```bash
# libftTester örneği
git clone https://github.com/Tripouille/libftTester.git
cd libftTester
make a
```

---

## 📖 Kaynaklar

- [42 Norm Kuralları](https://github.com/42School/norminette)
- [C Reference Manual](https://en.cppreference.com/w/c)
- [man7.org - Linux Manual Pages](https://man7.org/linux/man-pages/)

---

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakınız.

---

## 👤 İletişim

**42 Intra:** [malbayra]

**GitHub:** [@HalilAlb](https://github.com/HalilAlb)

---

<div align="center">

⭐ Bu proje faydalı olduysa yıldız vermeyi unutmayın!

Made with ❤️ at 42 School

</div>
