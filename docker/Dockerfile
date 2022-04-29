From alpine:3.10.3 as stage1
WORKDIR /
RUN touch stage1.txt

From alpine:3.10.3
COPY --from=stage1 /stage1.txt ./
CMD ["ls -l"]
