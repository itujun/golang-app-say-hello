## Repository Berkaitan

[golang-app-modules-hello](https://github.com/itujun/golang-app-modules-hello)

## Langkah-langkah

# Lanjutan Menambahkan Dependency

14. buka folder projek yang telah terbuat di pc/laptop (golang-app-say-hello) lalu ketik dan jalankan perintah:

```bash
go mod init github.com/itujun/golang-app-say-hello
```

15. panggil/get module yang sebelumnya telah terbuat di repository yang berkaitan. ketik dan jalankan di terminal:

```bash
go get github.com/itujun/golang-modules-say-hello
```

jika sukses, maka file go.mod akan menambahkan baris kode berikut:

```bash
require github.com/itujun/golang-modules-say-hello v1.0.0 // indirect
```

16. panggil method/func dari module yang telah terimport ke file main.go dengan kode berikut:

```bash
package main

import (
	"fmt"

	golang_modules_say_hello "github.com/itujun/golang-modules-say-hello"
)

func main() {
	fmt.Println(golang_modules_say_hello.SayHello())
}
```

17. test apakah func berhasil terpanggil. ketik dan jalankan di terminal:

```bash
go run main.go
```
