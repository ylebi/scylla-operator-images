FROM registry.access.redhat.com/ubi8/ubi-minimal:8.10-1018

SHELL ["/usr/bin/bash", "-euExo", "pipefail", "-O", "inherit_errexit", "-c"]

# Install a minimal subset of packages that *every* runtime image needs.
RUN microdnf update -y && \
    microdnf install -y curl ca-certificates jq && \
    microdnf clean all && \
    rm -rf /var/cache/dnf/*

ENTRYPOINT []
CMD ["/usr/bin/bash"]
