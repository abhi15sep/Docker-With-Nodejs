 ### Amazing Image Changer

 This command line app scans for images in ./in folder, 
 and turns them into chalk-looking images in ./out folder,
 then exits.

 It logs to two files in ./logs using Winston module

 It requires node v8.x

 The server need to have GraphicsMagick installed, so 
 you might need to do something like installing with apt:

 `apt-get install -y graphicsmagick`

 index.js is the main entrypoint


To run:
docker build -t mta .
docker run -v $(pwd)/in:/app/in -v $(pwd)/out:/app/out mta
docker run -v $(pwd)/in:/app/in -v $(pwd)/out:/app/out --env CHARCOAL_FACTOR=10 mta