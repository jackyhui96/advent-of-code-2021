# [Choice] alpine,...
# ARG VARIANT="alpine"
ARG VARIANT="latest"
# FROM erlang:${VARIANT}
FROM arm32v7/erlang:${VARIANT}

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=1001
ARG GRPNAME=vscodegrp

ENV DEBIAN_FRONTEND=noninteractive

# RUN addgroup -g $USER_GID $GRPNAME \
#     && adduser -u $USER_UID -g $GRPNAME -D $USERNAME
RUN addgroup --gid $USER_GID $GRPNAME \
    && adduser --uid $USER_UID $USERNAME \
    && adduser $USERNAME $GRPNAME

USER $USERNAME