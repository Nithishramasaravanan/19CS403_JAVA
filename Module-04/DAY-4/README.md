# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
You are developing a YouTube-like platform. Each channel can have multiple subscribers (viewers).

Whenever the channel uploads a new video, it must instantly notify all of its subscribers.

Each subscriber prints their own message like:

"[SubscriberName]: New video from [ChannelName]! Watching now..."

The channel doesn't care who the subscribers are or how many there are—it just broadcasts the update.

Student's Objective:
Implement the Observer Pattern:

Channel = Subject
Subscriber = Observer
When a video is uploaded, all subscribed users are notified.

Notifications should include channel name and video title.

Input Format:
First line: channelName

Second line: Integer n – number of subscribers

Next n lines: subscriber names

Next line: Integer v – number of videos uploaded

Next v lines: video titles

Output Format:
After each video upload:

[ChannelName] uploaded: [VideoTitle]
[SubscriberName]: New video from [ChannelName]! Watching now...
[SubscriberName]: New video from [ChannelName]! Watching now...
...

For example:
<img width="977" height="259" alt="image" src="https://github.com/user-attachments/assets/b1833fb9-0910-4a9a-914d-c3d0355e76f6" />



## AIM:
To write a Java program using the Observer Design Pattern where a YouTube channel (Subject) notifies all its subscribers (Observers) whenever a new video is uploaded.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the channel name from the user.
4.	Create a Channel (Subject) object.
5.	Read the number of subscribers n.
6. For each subscriber:Read the subscriber name,Create a Subscriber object,Add it to the Channel using subscribe().
7.	Read the number of videos v.
8.	For each video:Read the video title,Call uploadVideo() which-Prints upload message,Notifies every subscriber.
9.	Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: JESLIN GNANASHEELA M
RegisterNumber:  212222040062
*/
```

## SOURCE CODE:


```
import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;

    public Subscriber(String name) {
        this.name = name;
    }

    public void notify(String channelName, String videoTitle) {
        System.out.println(name + ": New video from " + channelName + "! Watch now...");
    }
}

class Channel {
    private String channelName;
    private List<Observer> subscribers;

    public Channel(String channelName) {
        this.channelName = channelName;
        this.subscribers = new ArrayList<>();
    }

    public void subscribe(Observer subscriber) {
        subscribers.add(subscriber);
    }

    public void uploadVideo(String videoTitle) {
        System.out.println(channelName + " uploaded: " + videoTitle);
        for (Observer sub : subscribers) {
            sub.notify(channelName, videoTitle);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String channelName = sc.nextLine();
        Channel channel = new Channel(channelName);
        int n = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }
        int v = sc.nextInt();
        sc.nextLine();
        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }
        sc.close();
    }
}

```




## OUTPUT:

<img width="1220" height="472" alt="image" src="https://github.com/user-attachments/assets/5afe579e-f12d-4f37-ad8a-7efa96a7503a" />



## RESULT:

The program successfully simulates a YouTube-like platform where a channel notifies its subscribers whenever a new video is uploaded.

