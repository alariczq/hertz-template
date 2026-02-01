# Hertz + FX Template

Custom hz template for generating Hertz projects with Uber FX dependency injection.

## Usage

```bash
# Create project
hz new --mod=github.com/xxx/xxx --service=xxx \
  --customize_layout=./hertz-template/layout.yaml \
  --customize_package=./hertz-template/package.yaml

# Generate IDL code
hz update --idl=idl/echo.proto \
  --customize_package=./hertz-template/package.yaml

# Run
go mod tidy && go run ./cmd/server
```

## Adding New Services

1. Create `idl/xxx.proto`
2. `hz update --idl=idl/xxx.proto --customize_package=...`
3. Implement `internal/service/xxx/*.impl.go`
