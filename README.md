# DL_homework

#### How to run:
1. Clone this repository.
    ```
    git clone https://github.com/Luab/DL_homework.git
    ```
2. Move to repository folder.
    ```
    cd DL_homework
    ```
3. Build the container.
    ```
    docker build . -t mnist
    ```
4. Run main.py to to train the model. (You can pass some parameters to model on this stage)
    ```
    docker run -v "*some path*":"/root/model" -it mnist  python main.py --epoch 1
    ```
   This will create model.nn file, which is pretrained model
   '''
4.5 Put data you want to predict on into your volume folder. Name it test.npy. It shoud match format expected by model
    '''
5. Run predict.py to start prediction.
    ```
    docker run -v "*some path*":"/root/model" -it mnist  python predict.py
    ```
