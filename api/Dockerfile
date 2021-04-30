FROM hayd/alpine-deno:1.9.2

RUN deno install -qAf --unstable https://deno.land/x/denon/denon.ts

WORKDIR /usr/app

COPY deps.ts .
RUN deno cache deps.ts

ADD . .

ENTRYPOINT ["/usr/local/bin/denon"]