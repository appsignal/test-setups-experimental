FROM node:15.5-buster

# Update this if the docker image changes
ENV REFRESHED_AT=2021-02-05

# Copy commands into the container
RUN mkdir /commands
COPY ./commands/* /commands/
RUN chmod +x /commands/*

# Run prepare and start processmon
CMD /commands/prepare && cd /app && /commands/processmon processmon.toml