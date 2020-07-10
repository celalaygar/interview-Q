# DESIGN PATTERN

### Observer (Gözlemci) Pattern
```
public interface Observer {
    void notify(String message);
}

public interface Observable {
    void addObserver(Observer observer);
    void removeObserver(Observer observer);
    void notifyObserver();
}
```
```
public class NoticeObservable implements Observable {

    private List<Observer> observerList = new ArrayList<>();
    private String message = "Notice... !";

    @Override
    public void addObserver(Observer observer) {
        observerList.add(observer); // Kullanıcıları duyuruya eklemek için.
    }

    @Override
    public void removeObserver(Observer observer) {
        observerList.remove(observer); // Kullanıcıları duyurudan silmek için.
    }

    @Override
    public void notifyObserver() {
        for (Observer observer : observerList) {
            observer.notify(message); // Duyuru ya kayıtlı kullanıcılara mesaj göndermek için.
        }
    }

}
```
```
public class UserMan implements Observer {

    private Observable observable;

    @Override
    public void notify(String message) {
        System.out.println(message + " UserMan Mesaj Geldi.");
    }

    public void removeObserver(){
        observable.removeObserver(this);
    }

}
```
```
public class UserWoman implements Observer {

    private Observable observable;

    public UserWoman() {
    }

    public void setObservable(Observable observable) {
        this.observable = observable;
    }

    @Override
    public void notify(String message) {
        System.out.println(message + " UserWoman Mesaj Geldi.");
    }

    public void removeObserver(){
        observable.removeObserver(this);
    }

}
```
```
public class Main {

    public static void main(String[] args) {

        UserMan userMan = new UserMan();
        UserWoman userWoman = new UserWoman();

        NoticeObservable noticeObservable = new NoticeObservable();

        userWoman.setObservable(noticeObservable);

        noticeObservable.addObserver(userMan);
        noticeObservable.addObserver(userWoman);
        noticeObservable.notifyObserver();

        userWoman.removeObserver();
        noticeObservable.notifyObserver();

    }
}
```
