Everything worked normally, though I had to keep browser's CORS protection disabled. For some reason it blocked http://localhost:8000 -> http://localhost:5000, thinking those are different URL's.

I don't know why that happens, but as that's not related to Docker and I'm not a frontend developer, nor intend to be, I just disabled CORS. Might have been because I needed SSH tunnel all traffic out of the VPS. 
