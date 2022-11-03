# Cours IPI JVA350 Qualité logicielle

## marp

```shell
# Server mode (Serve current directory in http://localhost:8080/)
docker run --rm --init -v $PWD:/home/marp/app -e LANG=$LANG -p 6080:8080 -p 37717:37717 marpteam/marp-cli -s .
http://localhost:6080/content.md
http://localhost:6080/content.md?pdf

# generate using CLI
cd ...
chmod -R 0777 . # anyone writes to, else error Failed converting Markdown. (EACCES: permission denied, open '/home/marp/app/content.pdf') https://github.com/marp-team/marp-cli/issues/79
docker run -u "node" --rm --init -v $PWD:/home/marp/app/ -e LANG=$LANG marpteam/marp-cli content.md (--pdf/pptx) --allow-local-files
# --allow-local-files else warning advices to upload them
# --allow-local-files else warning advices to upload them
```
