# go-gazelle-grpcgcp

This works fine:
```bash
go run main.go
```
This does not:
```bash
bazel run //:main
```
With an error like:
```bash
compilepkg: missing strict dependencies:
        /home/finn/.cache/bazel/_bazel_finn/dec216ef687f1bab8ce593af50f4cee9/sandbox/linux-sandbox/503/execroot/_main/external/gazelle~~go_deps~com_github_googlecloudplatform_grpc_gcp_go_grpcgcp/gcp_balancer.go: import of "github.com/GoogleCloudPlatform/grpc-gcp-go/grpcgcp/grpc_gcp"
        /home/finn/.cache/bazel/_bazel_finn/dec216ef687f1bab8ce593af50f4cee9/sandbox/linux-sandbox/503/execroot/_main/external/gazelle~~go_deps~com_github_googlecloudplatform_grpc_gcp_go_grpcgcp/gcp_multiendpoint.go: import of "github.com/GoogleCloudPlatform/grpc-gcp-go/grpcgcp/grpc_gcp"
        /home/finn/.cache/bazel/_bazel_finn/dec216ef687f1bab8ce593af50f4cee9/sandbox/linux-sandbox/503/execroot/_main/external/gazelle~~go_deps~com_github_googlecloudplatform_grpc_gcp_go_grpcgcp/gcp_picker.go: import of "github.com/GoogleCloudPlatform/grpc-gcp-go/grpcgcp/grpc_gcp"
No dependencies were provided.
Check that imports in Go sources match importpath attributes in deps.
Target //:main failed to build
Use --verbose_failures to see the command lines of failed build steps.
```
