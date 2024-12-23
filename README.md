# fuzzing-lighttpd

### Fuzz Lighttpd with AFLNet
```
cd aflnet
docker build -t aflnet-lighttpd --platform linux/amd64 .
docker run -it aflnet-lighttpd
./run.sh aflnet output-dir "-P HTTP -D 200000 -m none -q 3 -s 3 -E -K -R -t 20000+" 2000 1
```