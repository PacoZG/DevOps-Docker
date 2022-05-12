```yaml
version: '3.8'

services:
  frontend:
    image: frontend
    container_name: frontend
    build:
      context: ./frontend
      dockerfile: Dockerfile
    ports:
      - 3000:3000
  
  backend:
    image: backend
    container_name: backend
    build:
      context:  ./backend
      dockerfile: Dockerfile
    ports:
      - 5000:5000
    volumes:
      - model:/src/model
  
  training:
    image: training
    container_name: training
    build:
      context: ./training
      dockerfile: Dockerfile
    volumes:
      - model:/src/model
      - images:/src/imgs
      - data:/src/data

volumes:
  model:
  images:
  data:

```