# Graphviz

docker run -d -p 7777:7777 omerio/graphviz-server 7777

mkdir target
curl -X POST -d 'digraph G { a -> b -> c; a-> c; b -> d; c-> d; }' http://localhost:7777/bmp > target/output.bmp
curl -X POST --data-binary "@graph.dot" http://localhost:7777/bmp > target/output.bmp

Ref:
https://www2.graphviz.org
https://hub.docker.com/r/omerio/graphviz-server/
