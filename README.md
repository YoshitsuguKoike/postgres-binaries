# PostgreSQL Binaries for deespec

This repository contains pre-compiled PostgreSQL binaries with pgvector extension for the deespec project.

## Overview

These binaries enable deespec to provide an embedded PostgreSQL database without requiring users to install PostgreSQL separately.

## Included Components

- **PostgreSQL 16.11**: Full-featured PostgreSQL database
- **pgvector 0.8.1**: Vector similarity search extension

## Supported Platforms

- darwin-arm64 (macOS Apple Silicon - M1/M2/M3)

## Usage

These binaries are automatically downloaded during the deespec build process via the `download-postgres-binary.sh` script.

### Manual Download

```bash
# Download for macOS Apple Silicon
curl -L -o postgres-darwin-arm64.tar.gz \
  https://github.com/YoshitsuguKoike/postgres-binaries/releases/download/v16.11.0-pgvector-0.8.1/postgres-darwin-arm64.tar.gz

# Extract
tar -xzf postgres-darwin-arm64.tar.gz
```

## License

### PostgreSQL

PostgreSQL is released under the PostgreSQL License, a liberal Open Source license, similar to the BSD or MIT licenses.

```
PostgreSQL Database Management System
(formerly known as Postgres, then as Postgres95)

Portions Copyright © 1996-2024, The PostgreSQL Global Development Group

Portions Copyright © 1994, The Regents of the University of California

Permission to use, copy, modify, and distribute this software and its documentation for any purpose, without fee, and without a written agreement is hereby granted, provided that the above copyright notice and this paragraph and the following two paragraphs appear in all copies.

IN NO EVENT SHALL THE UNIVERSITY OF CALIFORNIA BE LIABLE TO ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES, INCLUDING LOST PROFITS, ARISING OUT OF THE USE OF THIS SOFTWARE AND ITS DOCUMENTATION, EVEN IF THE UNIVERSITY OF CALIFORNIA HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

THE UNIVERSITY OF CALIFORNIA SPECIFICALLY DISCLAIMS ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE SOFTWARE PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND THE UNIVERSITY OF CALIFORNIA HAS NO OBLIGATIONS TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.
```

### pgvector

pgvector is released under the PostgreSQL License.

```
Copyright (c) 2021-present, Andrew Kane

Permission to use, copy, modify, and distribute this software and its documentation for any purpose, without fee, and without a written agreement is hereby granted, provided that the above copyright notice and this paragraph and the following two paragraphs appear in all copies.

IN NO EVENT SHALL THE COPYRIGHT HOLDER BE LIABLE TO ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES, INCLUDING LOST PROFITS, ARISING OUT OF THE USE OF THIS SOFTWARE AND ITS DOCUMENTATION, EVEN IF THE COPYRIGHT HOLDER HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

THE COPYRIGHT HOLDER SPECIFICALLY DISCLAIMS ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE SOFTWARE PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND THE COPYRIGHT HOLDER HAS NO OBLIGATIONS TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.
```

## Build Information

Binaries are built from official Homebrew packages:
- `postgresql@16` (16.11)
- `pgvector` (0.8.1)

## Security

These binaries are provided as-is for development and production use. Please ensure you:
- Verify checksums after download
- Keep PostgreSQL updated with security patches
- Follow PostgreSQL security best practices

## Contributing

To add support for additional platforms, please:
1. Build PostgreSQL 16.11 with pgvector 0.8.1 for your platform
2. Create a tar.gz archive with the same structure
3. Submit a pull request with the release

## Links

- [deespec Project](https://github.com/YoshitsuguKoike/deespec)
- [PostgreSQL Official Site](https://www.postgresql.org/)
- [pgvector GitHub](https://github.com/pgvector/pgvector)
