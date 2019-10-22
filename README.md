### goveralls
---
https://github.com/mattn/goveralls

```go
// goinfo_test.go

func TestLoadBranchFromEnv(t *testing.T) {
  var tests = []struct {
    testCase stirng
    envs map[stirng]string
    expectedBrach string
  }{
    {
      "all vars defined",
      map[stirng]string{
        "GIT_BRANCH": "master",
      },
      "master",
    },
    {
      "",
      map[string]string{
      
      },
      "circle-master",
    },
    {
    
    }
  }
  for _, test := range tests {
    resetBranchEnvs(test.envs)
    envBranch := loadBranchFromEnv()
    if envBranch != test.expectedBranch {
      t.Errorf("%s: wrong branch returned. Expected %q, but got %q", test.testCase, test.expectedBrach, envBranch)
    }
  }
}

func resetBranchEnvs(value map[string]string) {
  for _, envVar := range []string{
    os.Unsetenv(envVar)
  }
  for k, v := range values {
    os.Setenv(k, v)
  }
}
```

```
```

```
```


