# Scalable-AI-Systems-for-Real-World-Applications

## Batch prediction

This help improve performance of system. Because normaly, each model can predict in batch.

The main idea is store incomming request and wait for at least one of these following condition is satisfied:

- The number of request reach threshold (batch size)

- The timeout exceed

To response to exact client, there are 2 ways:

- Using socket

- Client send 2 request (1 for send request for making prediction, 1 is a long poll request send immediately after the first one to get the prediction result)

