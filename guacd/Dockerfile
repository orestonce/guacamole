FROM guacamole/guacd

#https://github.com/StellarCN/scp_zh/blob/master/fonts/SimHei.ttf
COPY ./fonts/Menlo-Regular.ttf /usr/share/fonts/
COPY ./fonts/SourceHanSansCN-Regular.otf /usr/share/fonts/
RUN mkfontscale && mkfontdir && fc-cache
