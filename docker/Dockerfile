From alpine:3.10.3 as stage1
WORKDIR /
RUN echo "stage" > stage1.txt

From python:3.7.5-slim as stage2
RUN pip install flask==1.1.1
WORKDIR /
RUN touch stage2.txt

From alpine:3.10.3
COPY --from=stage1 /stage1.txt ./
COPY --from=stage2 /stage2.txt ./
CMD ["ls -l"]
