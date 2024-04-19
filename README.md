# Yolo_login_project

# FastAPI + YOLO 프로젝트

# 주제 : 사용자의 얼굴을 학습시킨 후 학습된 데이터를 바탕으로 현재 사용자가 등록된 사용자인지 확인한다.

# 구현 기능
## 1. Backend : FastAPI
    - 로그인 : 사용자의 얼굴을 확인하여 등록된 사용자인지 확인
    - 사용자 맞춤 페이지 : 로그인에 성공한 경우 각 사용자에 맞는 페이지로 이동
    - 경고 페이지 : 로그인에 실패한 경우 인증된 사용자가 아니라는 페이지로 이동 -> 옵션 : 새로운 사용자 등록

## 2. 사용자 얼굴 학습
    - 사용자 얼굴 이미지 수집
    - labelimg를 사용하여 라벨링
    - colab에서 yolo 학습
    - 학습 결과 파일 생성

## 3. Frontend : svelte
    - login : 사용자의 얼굴 촬영 -> 학습 결과 파일을 사용하여 사용자 확인
    - 사용자 맞춤 페이지 : 로그인한 사용자에따라 다른 페이지로 이동
    - 로그인 실패 페이지 : 등록되지 않은 사용자라는 에러 표시 -> 옵션 : 사용자 등록 페이지 -> 새롭게 학습을 해야되는데 일단 보류

## 4. EC2
    - AWS EC2를 사용하여 퍼블릭

## 파일 구조

| — yolo 학습 파일

| — domain

|           | — router.py

|           | — crud.py

|           | — schema.py

| — database.py

| — models.py

| — main.py
