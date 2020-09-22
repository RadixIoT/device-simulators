FROM python:3.7-slim

RUN pip install snmpsim

RUN adduser --system snmpsim

RUN mkdir -p /usr/local/snmpsim/data
RUN chown -R snmpsim:nogroup /usr/local/snmpsim

EXPOSE 161/udp

CMD snmpsimd.py --agent-udpv4-endpoint=0.0.0.0:161 --process-user=root --process-group=root $EXTRA_FLAGS
