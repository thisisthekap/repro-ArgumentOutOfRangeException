# repro-ArgumentOutOfRangeException
Reproduction for a Xamarin.Android Bindings Generator ArgumentOutOfRangeException issue created at https://github.com/xamarin/java.interop/issues/728.

## Repro steps:

```bash
git clone https://github.com/thisisthekap/repro-ArgumentOutOfRangeException.git
cd repro-ArgumentOutOfRangeException
msbuild /t:Restore
cd purchases-core-common
msbuild /t:Build -verbosity:diagnostic
```

The build fails, now search the build output for `System.ArgumentOutOfRangeException`.
