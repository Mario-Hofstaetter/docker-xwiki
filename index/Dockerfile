ARG SOLR_VERSION
FROM busybox as build

# ARGs for Build MUST be after the FROM statement!
ARG XWIKI_VERSION
ARG XWIKI_URL_PREFIX="http://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-search-solr-server-data/${XWIKI_VERSION}"

WORKDIR /var/xwiki-solr-temp/

COPY ./solr-init.sh .
RUN wget "${XWIKI_URL_PREFIX}/xwiki-platform-search-solr-server-data-${XWIKI_VERSION}.jar"

FROM solr:${SOLR_VERSION}

COPY --from=build /var/xwiki-solr-temp/ /docker-entrypoint-initdb.d/

