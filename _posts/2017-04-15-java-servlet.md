---
layout: post
title: 자바 서블릿(Java Servlet)의 정의와 라이프사이클에 대해서
---

서블릿이란 클라이언트의 요청을 처리하고 그 결과를 반환하는 자바 서블릿 API 규약을 따르는 서버 프로그램을 말한다. 모든 종류의 요청에 대해 처리할수 있지만 일반적으로 HTTP 요청을 처리하기 위해 사용된다. 

서블릿 API는 javax.servlet 패키지에 정의되어 있다.

서블릿의 라이프사이클은 init(), service(), destroy() 세개의 메쏘드에 의해 관리된다. 

# 라이프사이클 
> 서블릿 컨테이너를 어떻게 구현했느냐에 따라 차이는 있다.

1. 클라이언트(사용자)가 URL을 통해 요청을 한다.
1. 웹서버는 요청을 받아서 서블릿 컨테이너에게 전달한다.
1. 컨테이너는 요청을 처리할 서블릿을 메모리 공간에 로드한다.
1. 메모리에 서블릿이 로드되면 컨테이너는 init()을 호출해서 초기화한다.
1. service()를 호출해서 HTTP request를 처리한 다음 그 결과를 HTTP response에 실어서 클라이언트에게 반환한다.
1. destroy()를 호출해서 리소스를 정리하고 메모리에 있는 서블릿은 GC가 이루어 진다.





