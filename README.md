# Aspose.BarCode Cloud SDKs: test coverage

Line coverage of every [Aspose.BarCode Cloud SDK](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-codegen),
published by each SDK's CI on every push to its default branch. The required minimum is 80%.

| SDK | Coverage | Repository |
|-----|----------|------------|
| .NET | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/dotnet/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-.NET](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-.NET) |
| Dart | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/dart/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-Dart](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-Dart) |
| Go | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/go/coverage-badge.json) | [aspose-barcode-cloud-go](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-go) |
| Java | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/java/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-Java](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-Java) |
| Node.js | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/node/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-Node.js](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-Node.js) |
| PHP | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/php/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-PHP](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-PHP) |
| Python | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/python/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-Python](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-Python) |
| Swift | ![Coverage](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/aspose-barcode-cloud/test-coverage/main/swift/coverage-badge.json) | [Aspose.BarCode-Cloud-SDK-for-Swift](https://github.com/aspose-barcode-cloud/Aspose.BarCode-Cloud-SDK-for-Swift) |

## Layout

One folder per SDK: `dart`, `dotnet`, `go`, `java`, `node`, `php`, `python`, `swift`.

| File | Content |
|------|---------|
| `coverage-badge.json` | [shields.io endpoint](https://shields.io/badges/endpoint-badge) document behind the badge above |
| `summary.json` | percent, covered and total lines, threshold, SDK commit, workflow run URL, date |
| `lcov.info`, `coverage.xml`, `clover.xml`, `jacoco.xml`, `coverage.out` or `codecov.json` | the native coverage report of the SDK's tooling |

Each publish is one commit, so `git log -- <sdk>/summary.json` is the coverage history of that SDK.

## How it is written

`make cover` in every SDK measures line coverage with the SDK's native tool and the shared
`scripts/coverage.py`. A separate `publish-coverage` job in the SDK's workflow then commits the result here,
using a GitHub App installed only on this repository. Details:
[test coverage requirements](https://github.com/aspose-barcode-cloud/aspose-barcode-cloud-codegen/blob/main/doc/test-coverage-requirements.md).

Nothing here is edited by hand.
