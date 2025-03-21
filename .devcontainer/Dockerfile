FROM rocker/shiny:latest

# Install additional R packages
RUN install2.r --error \
    ggplot2 \
    dplyr \
    tidyr

# Expose Shiny's default port
EXPOSE 3838

# Set up the working directory
WORKDIR /workspace

CMD ["R", "-e", "shiny::runApp('/workspace', host = '0.0.0.0', port = 3838)"]
