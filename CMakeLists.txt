cmake_minimum_required(VERSION 3.22)
cmake_policy(SET CMP0135 NEW)

project(
  JUCEDirect2DTest
  VERSION 0.0.0
  LANGUAGES C CXX)

include(FetchContent)
FetchContent_Declare(
  juce
  URL https://github.com/juce-framework/JUCE/archive/refs/heads/direct2d.zip)
FetchContent_MakeAvailable(juce)

juce_add_pip("libs/JUCEDirect2DTest/PIPs/SimpleFFTDemo/Source/SimpleFFTDemo.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Brush Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Cached Path Creation Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D FlexBox Animation.h")
# juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Font Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Image Draw Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Image Edit Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Direct2D Path Draw Test.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Many Components.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Particles.h")
juce_add_pip("libs/JUCEDirect2DTest/PIPs/Select Renderer.h")

# juce_add_pip("libs/JUCEDirect2DTest/PIPs/SimpleFFTDemo.h")
# juce_add_pip("libs/JUCEDirect2DTest/PIPs/StatTable.h")

add_compile_definitions(JUCE_DIRECT2D_METRICS)
