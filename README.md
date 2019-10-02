# Read JPEG quality from bytes or os.File

Inpiration from [Estimating Quality](http://fotoforensics.com/tutorial-estq.php)


## code usage:

````go

	file, err := os.Open("file.jpg")
	if err != nil {
		log.Fatal(err)
	}
	j, err := jpegquality.New(file) // or NewWithBytes([]byte)
	if err != nil {
		log.Fatal(err)
	}
	log.Printf("jpeg quality %d", j.Quality())
````

## cli tool

```sh
go get github.com/liut/jpegquality/cmd/jpegq
```
