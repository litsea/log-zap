# logger

Initial logger by [viper](https://github.com/spf13/viper)

## Quick Start

```go
viper.SetConfigName("config")
viper.AddConfigPath(".")
if err := viper.ReadInConfig(); err != nil {
    fmt.Println("read config failed: ", err)
    os.Exit(1)
}

v := viper.Sub("log")
if err := logger.NewLogger(v, logger.DriverZap); err != nil {
    fmt.Println("init logger failed: ", err)
    os.Exit(1)
}

logger.Info("Logger initialized")
```

## Log driver

* [zap](https://github.com/uber-go/zap)

## Configuration

see: [config.yml](config.yml)
