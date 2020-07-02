
	private washrool washrool1;
	public RepairTask(washrool washrool2){
		this.washrool1=washrool2;
	}
	@Override
	public void run() {
		// TODO Auto-generated method stub
		synchronized(washrool1.getloke()){
		System.out.println("维修工正在维修厕所");
		System.out.println("厕所堵住太严重了看来要很长一段时间");
		
		try {
			Thread.sleep(1000);
		} catch (InterruptedException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
		washrool1.setisAvaible(true);	//设置厕所为可以
		washrool1.getloke().notifyAll();			//将同步的等待线程全程开启
		System.out.println("厕所终于通了");
			
		}
	}
