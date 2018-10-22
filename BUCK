genrule(
  name = 'core-foundation-framework', 
  out = 'CoreFoundation.framework', 
  cmd = 'cp -r /System/Library/Frameworks/CoreFoundation.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'core-foundation', 
  framework = ':core-foundation-framework', 
  preferred_linkage = 'static', 
)

genrule(
  name = 'cocoa-framework', 
  out = 'Cocoa.framework', 
  cmd = 'cp -r /System/Library/Frameworks/Cocoa.framework $OUT', 
)

prebuilt_apple_framework(
  name = 'cocoa', 
  framework = ':cocoa-framework', 
  preferred_linkage = 'static', 
)

cxx_binary(
  name = 'main', 
  srcs = [
    'main.cpp', 
  ], 
  deps = [
    ':core-foundation', 
    ':cocoa', 
  ], 
)

# apple_binary(
#   name = 'main', 
#   srcs = [
#     'main.cpp', 
#   ], 
#   frameworks = [
#     '$SDKROOT/System/Library/Frameworks/CoreFoundation.framework',
#     '$SDKROOT/System/Library/Frameworks/Cocoa.framework',
#   ], 
# )
