scala_library(name='larry',
  sources=['Larry.scala'],
  strict_deps=True,
)

jvm_binary(name='larry-bin',
  basename='larry',
  main='larry.Larry',
  dependencies=[
    ':larry',
    'src/javascript:js-module',
  ]
)
