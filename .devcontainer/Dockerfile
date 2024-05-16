# Node.js 20 이미지를 기반으로 설정
FROM node:20

# ARG USERNAME=vscode
# ARG USER_UID=1000
# ARG USER_GID=$USER_UID

ARG SSH_PRIVATE_KEY="default"
RUN echo "SSH_PRIVATE_KEY : ${SSH_PRIVATE_KEY}"

# RUN apt-get -y update && apt-get -y install \
#       curl \
#       ca-certificates \
#       screen \
#       net-tools \
#       && apt-get autoremove -y \
#       && apt-get clean -y

# USER $USERNAME

# 작업 디렉토리 설정
WORKDIR /workspace

# 필요한 패키지 설치
COPY package.json yarn.lock ./
RUN yarn install

# 전체 프로젝트 복사
# COPY . .

# Zsh 및 Oh My Zsh 설정 스크립트 복사 및 실행
COPY .devcontainer/setup-zsh.sh /tmp/setup-zsh.sh
RUN sh /tmp/setup-zsh.sh

# 개발 서버 실행
# CMD ["yarn", "dev", "--host"]
CMD [ "/bin/bash" ]
