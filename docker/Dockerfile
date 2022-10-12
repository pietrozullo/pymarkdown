FROM python3.8

# Install Driving Games risk
WORKDIR /pymarkdown
RUN pip install --upgrade pip

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

RUN find .

ENV DISABLE_CONTRACTS=1

#RUN pipdeptree
RUN python setup.py develop --no-deps

RUN risk-exp --help

RUN crash-exp --help

CMD ["risk-exp"]