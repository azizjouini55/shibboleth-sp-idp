FROM osixia/openldap:latest



# Copy the script for adding users to LDAP directory
COPY ds-setup.inf /ds-setup.inf
COPY users.ldif /users.ldif



# Set permissions on the LDIF and script files
USER root
RUN chown -R openldap:openldap /container/service/slapd/assets/config/bootstrap/ldif/
RUN chmod 400 /container/service/slapd/assets/config/bootstrap/ldif/*
RUN chown openldap:openldap /ds-setup.inf
RUN chown openldap:openldap /users.ldif

# Expose LDAP ports
EXPOSE 389 636

