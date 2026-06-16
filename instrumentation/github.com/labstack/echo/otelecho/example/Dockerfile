# Copyright The OpenTelemetry Authors
# SPDX-License-Identifier: Apache-2.0
FROM golang:alpine@sha256:f1ddd9fe14fffc091dd98cb4bfa999f32c5fc77d2f2305ea9f0e2595c5437c14 AS base
COPY . /src/
WORKDIR /src/instrumentation/github.com/labstack/echo/otelecho/example

FROM base AS echo-server
RUN go install ./server.go
CMD ["/go/bin/server"]
