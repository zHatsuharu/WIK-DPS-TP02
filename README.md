# WIK-DPS-TP02

## Requirements

- OS : Linux (everything was made on Manjaro)
- Docker

## How it works ?

- First, clone the repo 
    - `git clone https://github.com/zHatsuharu/WIK-DPS-TP02.git`

You have 2 images available :
- In `/tp-02-docker1`, you have a single stage image with a user.
- In `/tp-02-docker2`, you have a multi stage image.

To have both images, type this :
```bash
> cd tp-02-docker1
tp-02-docker1> docker build -t tp02docker1 .
tp-02-docker1> cd ../tp-02-docker2
tp-02-docker2> docker build -t tp02docker2 .
```

Now to run the image, just do :
```bash
> docker run --rm -it --network="host" <Image Name>
```
> Replace `<Image Name>` by `tp02docker1` or `tp02docker2`

## Result
Open your browser and go to `localhost:8080/ping`

You can curl it with :
```bash
curl -v localhost:8080/ping
```

> You have a trivy scan result in the `scan.txt` file.