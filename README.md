# RMI
RMI ( Remote Method Invocation) Menggunakan Java Sederhana

## I. PENDAHULUAN ##
Remote Method Invocation (RMI) adalah mekanisme dalam bahasa pemrograman Java yang memungkinkan objek yang berjalan di satu mesin Java Virtual Machine (JVM) untuk memanggil metode pada objek lain yang berada di JVM berbeda, baik di jaringan lokal maupun melalui internet. Dengan menggunakan RMI, pengembang dapat membuat aplikasi yang mendistribusikan pemrosesan antara beberapa server dan klien, sehingga memungkinkan pemisahan logika bisnis dan client secara efisien.

<p>Fitur </p>
<p>1.Cek Saldo </p>
<p>2.Tranfer Dana</p>
<p>3.Penarikan Tanpa Kartu</p>
<p>4. Lihat Riwayat Transaksi</p>
<p>5. Keluar</p>

## II. PENJELASAN KODE ##
** Interface ('Bank.java')**
''' java
  import java.rmi.Remote;
import java.rmi.RemoteException;
import java.util.List;

public interface Bank extends Remote 
{

    double checkBalance(String accountNo, String pin) throws RemoteException;

    boolean transferFunds(String fromAccount, String toAccount, double amount, String pin) throws RemoteException;

    List<String> getTransactionHistory(String accountNo, String pin) throws RemoteException;

    boolean login(String accountNo, String pin) throws RemoteException;

    // Method untuk penarikan tanpa kartu
    boolean cardlessWithdraw(String uniqueCode, double amount) throws RemoteException;
}
'''



