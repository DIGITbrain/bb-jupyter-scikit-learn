FROM python:3-slim

ENV PATH=/root/.local/bin:$PATH

# Install the required stack
RUN pip install --user "jupyterlab>=4,<5" \
    "scikit-learn>=1,<2" \
    pandas \
    numpy \
    matplotlib

EXPOSE 8888

ENV JUPYTER_PASSWORD=jupyterlab

COPY ./scikit-learn.ipynb /example/
COPY ./docker-entrypoint.sh /

ENTRYPOINT ["/docker-entrypoint.sh"]

CMD ["--allow-root", "--no-browser", "--ip=0.0.0.0", "--port=8888", "--config=/var/lib/jupyter/jupyter_lab_config.py", "--notebook-dir=/example"]
