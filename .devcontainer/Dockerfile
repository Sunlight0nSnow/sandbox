FROM homebrew/brew

ARG TERRAFORM_VERSION="0.11"
ARG ANSIBLE_VERSION="2.9.9"

ARG TERRAFORM_PACKAGE_NAME="terraform@$TERRAFORM_VERSION"

RUN brew install python

RUN pip3 install --upgrade pip && \
    pip3 install ansible==$ANSIBLE_VERSION

RUN brew install $TERRAFORM_PACKAGE_NAME \
    && mv /home/linuxbrew/.linuxbrew/opt/$TERRAFORM_PACKAGE_NAME/bin/terraform /usr/local/bin/terraform
