FROM debian:stable-20221114
RUN echo "deb http://deb.debian.org/debian bullseye-backports main" > /etc/apt/sources.list.d/backports.list && \
apt update && \
apt install -y git curl && \
curl -sL https://deb.nodesource.com/setup_18.x -o /tmp/nodesetup.sh && \
bash /tmp/nodesetup.sh && \
apt install -y nodejs && \
node -v && \
mkdir -p /app/src && \
cd /app/src && \
git clone https://github.com/kusa-mochi/compare-frontend-frameworks.git
EXPOSE 80
EXPOSE 443
CMD ["/bin/bash"]