# DDownloader
##  Usage
- Download Content:
  
	```python
	from DDownloader.modules.downloader import DOWNLOADER

	downloader = DOWNLOADER()
	downloader.manifest_url = "https://example.com/path/to/manifest"  # DASH, HLS, or ISM manifest URL
	downloader.output_name = "output.mp4"  # Desired output file name
	downloader.decryption_keys = ["12345:678910"]  # Provide decryption keys if needed
	downloader.download()  # Start the downloading and decryption process
	```
 
- Extract Media Information:
  
	```python
	from DDownloader.modules.helper import get_media_info

	file_path = "downloads/example.mp4"
	media_info = get_media_info(file_path)
	print(media_info)
	```

- Re-encoding:

	```python
	from DDownloader.modules.downloader import DOWNLOADER

 	re_encode = DOWNLOADER()
	quality = ["HD", "FHD", "UHD"]
	input_content = "downloads/example.mp4"
	output_content = "/path/to/output.mp4"
 	re_encode.re_encode_content(input_file=input_content,quality=quality,codec="libx265",crf=20,preset="medium")
	```
  
## CLI Usage
- Download Media
  
	```bash
	DDownloader -u https://example.com/path/to/manifest -o output.mp4
	```
 
- Specify Decryption Keys
  
	```bash
	DDownloader -u https://example.com/path/to/manifest -o output.mp4 -k 12345:678910
	```

- Re-encoding

	```bash
 	DDownloader -i "input.mp4" -o "output.mp4" -q "HD, FHD, UHD"
 	```


- Display Help
  
	```bash
	DDownloader -h
	```

- ![image](https://github.com/user-attachments/assets/8c73a79e-fcac-4bde-a07c-5628db0d19df)


## THIS PROJECT STILL IN DEVELOPMENT
- Contributions are welcome! Feel free to open issues, create pull requests, or provide suggestions.
