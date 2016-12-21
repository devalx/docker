FROM node:6

ENV ANGULAR_CLI_VERSION latest

RUN npm -g install yarn --quiet \
	&& yarn global add angular-cli@${ANGULAR_CLI_VERSION} \
	&& node --version
	&& yarn version 